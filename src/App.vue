<template>
  <div id="app">
    <Generator />
    <Footer />
  </div>
</template>

<script>
import Generator from './components/Generator.vue';
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Generator,
    Footer,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2a4c6d;
  margin-top: 0;
  background: #fff5f2;
  height: 100vh;
  padding: 100px 100px 50px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-sizing: border-box;
}
</style>
