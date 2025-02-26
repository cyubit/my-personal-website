<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Website Logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="Ali Habash" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/more">More</RouterLink>
      </nav>
    </div>
  </header>

  <div>
    <RouterView />
  </div>

  <footer>Uicons by <a href="https://www.flaticon.com/uicons">Flaticon</a></footer>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  position: sticky;
  top: 0;
}

footer {
  position: fixed;
  bottom: 0;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  /* Recolors the logo by filtering over it. https://codepen.io/sosuke/pen/Pjoqqp */
  filter: var(--filter-brunswick);
}

nav {
  width: 100%;
  font-size: 1.4rem;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--text-selected);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  color: var(--text-secondary);
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
