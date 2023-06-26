<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>|
    <router-link to="/projects">Projects</router-link> |
    <router-link to="/contact">Contact</router-link> |
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  background-color: #000000;
}

nav a {
  font-weight: bold;
  color: #414bb4;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #365abb;
}


</style>
