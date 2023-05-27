<template>
  <div class="bg">
    <div id="app">
      <div id="nav">
        <Navigator msg="Cruith.net" />
      </div>
      <router-view id="route" />
    </div>
  </div>
</template>

<script lang="ts">
import Navigator from "./views/Navigator.vue";
export default {
  name: "App",
  components: {
    Navigator,
  },
};
</script>

<style>
.bg {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-image: url("./assets/background.png");
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  
  margin: 0 auto;
}


#route {
  justify-content: center;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
