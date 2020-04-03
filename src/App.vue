<template>
  <div id="app">
    <Generator />
  </div>
</template>

<script>
import Generator from './components/Generator.vue';

export default {
  name: 'App',
  components: {
    Generator,
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
  margin-top: 0;
  background: #fff5f2;
  height: 100vh;
  padding: 100px;
}
</style>
