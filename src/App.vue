<template>
  <div id="app">
    <ContainerQueries />
  </div>
</template>

<script>
import ContainerQueries from "./components/ContainerQueries.vue";

export default {
  name: "App",
  components: {
    ContainerQueries,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
