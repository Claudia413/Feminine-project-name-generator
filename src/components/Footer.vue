<template>
  <footer>
    <p>
      Made by
      <a href="https://www.claudiaengelsman.com/" target="_blank" rel="noopener"
        >Claudia Engelsman</a
      >
      with
      <a href="https://vuejs.org/" target="_blank" rel="noopener"><i class="fab fa-vuejs"></i></a>
      and
      <a href="https://fontawesome.com/" target="_blank" rel="noopener"
        ><i class="fab fa-font-awesome"></i></a
      >, stored on
      <a
        href="https://github.com/Claudia413/Feminine-project-name-generator"
        target="_blank"
        rel="noopener"
        ><i class="fab fa-github"></i></a
      >, and hosted by
      <a href="https://www.netlify.com/" target="_blank" rel="noopener">Netlify</a>.
    </p>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
a {
  color: #2a4c6d;
  text-decoration: none;
  transition: 0.3s color ease-out;
  &:hover {
    color: #5499dd;
  }
}
</style>
