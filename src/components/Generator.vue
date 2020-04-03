<template>
  <div class="flex">
    <h1>A feminine project name generator</h1>
    <MagicButton />
  </div>
</template>

<script>
import MagicButton from './MagicButton.vue';

export default {
  name: 'Generator',
  components: {
    MagicButton,
  },
};
</script>

<style scoped lang="scss">
  .flex {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>
