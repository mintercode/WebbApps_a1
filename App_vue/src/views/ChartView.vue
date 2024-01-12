<script setup>
import TelemetryChart from '@/components/TelemetryChart.vue';
</script>

<template>
  <div class = "Charts-Page">
    <!-- Your other content -->
    <TelemetryChart></TelemetryChart>
  </div>
</template>

<style scoped>

.fancy {
  font-weight: 700;
  font-size: 48px;
  color: yellow;
  font-style: italic;
}

.chart-info{
  min-height: 100vh;
  display: flex;
  align-items: center;
}


</style>
