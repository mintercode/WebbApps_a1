<template>
<div class="about-container">
    <div class="about-text">
      <h1>Hello We Are Team Mysticat</h1>
      <p>
         A group of VFS students working on our game Catatonic, this is our Live Op's
         site for internal use to track metrics in our game for development purposes 
      </p>
    </div>
  </div>
</template>

<style>
.grid-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 0.5rem; /* Adjust overall padding around the grid */
  gap: 1rem; /* Space between items */
}

.home-pic {
  flex-basis: calc(50% - 1rem); /* Half the width minus the gap */
  display: flex;
  justify-content: center;
  align-items: center;
}

.home-pic img {
  width: 100%; /* Adjust width as needed */
  height: auto; /* Maintain aspect ratio */
  object-fit: contain; /* Ensures the image fits within the container */
}

@media (min-width: 1024px) {
  .grid-container {
    /* Adjust styles for larger screens if needed */
  }
}
</style>
