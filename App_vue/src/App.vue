<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Welcome from '@/components/TheWelcome.vue'; // Adjust the path as per your project structure
</script>
<template>
  <nav>
    <div class = "Title">CATATONIC</div>
        <RouterLink to="/home">Home</RouterLink>
        <RouterLink to="/charts">Charts</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.Title{
  font-size: 65px
}

.logo {
  display: flex;
  flex-direction: column;
  width: 20rem;
  height: 20rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
