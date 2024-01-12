<template>
  <div class="about-container">
    <div class="about-text">
      <h1>The Game</h1>
      <p>
        A group of VFS students working on our game Catatonic, a 2.5D High Fantasy Noir Dungeon Crawler.
         Features include Magic Saxophone Combat: Players cast spells using a magic saxophone, as well as a 
         High Fantasy Noir Setting: A blend of high fantasy elements with dark mysterious noir themes. Players will have to master spell combinations and 
         strategic use of the magic saxophone. 
        
      <img src="@/assets/level-cat.png" alt="Cat Image 1" />
      </p>
      <h1>The Mysticat Team</h1>
       <p>
         We are a group of VFS students working on our team project Catatonic.  <br>
         <br>
         Connor - PM / All Rounder
         <br>
         Cameron - Programmer / Audio
         <br>
         Jake - Level Designer / Chardian
         <br>
         Tommy - Programmer / Build Master
         <br>
         Sergio - Artist 
      </p>
    </div>
  </div>
  
</template>

<style>
.about-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
}

.about-image {
  width: 100%; /* Adjust width as needed */
  max-width: 600px; /* Maximum image width */
  margin-bottom: 1rem; /* Space between image and text */
}

.about-text h1, .about-text p {
  margin: 0;
  padding: 0;
}

@media (min-width: 1024px) {
  .about-container {
    flex-direction: row;
    align-items: start;
  }

  .about-image {
    width: 50%;
    margin-right: 2rem; /* Space between image and text */
  }

  .about-text {
    width: 50%;
  }
}
</style>
