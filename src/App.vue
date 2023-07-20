<template>
  <app-nav-bar></app-nav-bar>

  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <app-footer></app-footer>
  <router-view />
</template>
<script>
import AppNavBar from "./components/AppNavBar.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  components: {
    AppNavBar,
    AppFooter,
  },
};
</script>

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
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
