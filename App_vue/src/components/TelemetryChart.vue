<template class = "chart-page">
  <div class="chart-container">
    <div class="chart-row">
      <div class="mini-chart chart-border" ref="chart1"></div>
      <div class="mini-chart chart-border" ref="chart2"></div>
    </div>
    <div class="chart-row">
      <div class="mini-chart chart-border" ref="chart3"></div>
      <div class="mini-chart chart-border" ref="chart4"></div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const chart1 = ref(null);
const chart2 = ref(null);
const chart3 = ref(null);
const chart4 = ref(null);

onMounted(() => {
  google.charts.load('current', { 'packages': ['corechart'] });
  google.charts.setOnLoadCallback(drawCharts);
});

function drawCharts() {
  // Chart 1: Kills (BarChart)
  drawSpecificChart(chart1.value, {
    data: [['Type', 'Number'], ['Player Kills', 120], ['Enemy Kills', 200]],
    options: { title: 'Kills' }
  }, 'BarChart');

  // Chart 2: Time Spent In Game (PieChart)
  drawSpecificChart(chart2.value, {
    data: [['Session', 'Hours'], ['Short (<1h)', 1000], ['Long (>1h)', 1170]],
    options: { title: 'Time Spent In Game' }
  }, 'PieChart');

  // Chart 3: User Details (ColumnChart)
  drawSpecificChart(chart3.value, {
    data: [['Category', 'Number'], ['Age 18-24', 400], ['Age 25-34', 600]],
    options: { title: 'User Details' }
  }, 'ColumnChart');

  // Chart 4: Player Retention (LineChart)
  drawSpecificChart(chart4.value, {
    data: [['Time', 'Retention Rate'], ['Week 1', 80], ['Week 2', 60]],
    options: { title: 'Player Retention' }
  }, 'LineChart');
}

function drawSpecificChart(container, dataOptions, chartType) {
  const data = google.visualization.arrayToDataTable(dataOptions.data);
  let chart;

  if (chartType === 'BarChart') {
    chart = new google.visualization.BarChart(container);
  } else if (chartType === 'PieChart') {
    chart = new google.visualization.PieChart(container);
  } else if (chartType === 'ColumnChart') {
    chart = new google.visualization.ColumnChart(container);
  } else if (chartType === 'LineChart') {
    chart = new google.visualization.LineChart(container);
  }
  
  chart.draw(data, dataOptions.options);
}

</script>

<style scoped>
.chart-container {
  display: flex;
  flex-direction: column;
  gap: 1rem; /* Adjust the space between rows */
}

.chart-row {
  display: flex;
  justify-content: space-between; /* space out the charts in a row */
  gap: 1rem; /* Adjust the space between charts in a row */
}

.mini-chart {
  width: 20rem;
  height: 20rem;
}

.chart-border {
  border: 2px solid white;
}
</style>
