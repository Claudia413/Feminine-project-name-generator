<template>
  <div class="flex">
    <h1>A feminine project name generator</h1>
    <div class="inline">
      {{name}}
      <MagicButton v-on:generate="generateName()" />
    </div>
  </div>
</template>

<script>
import MagicButton from './MagicButton.vue';
import Words from '@/assets/words.json'

export default {
  name: 'Generator',
  components: {
    MagicButton,
  },
  data () {
    return {
      words: Words,
      name: ""
    }
  },
  methods: {
      getRandomNumber(max) {
        return Math.floor(Math.random() * max);
      },
      generateName() {
        this.name = this.words.firstWord[this.getRandomNumber(this.words.firstWord.length)] + '-' + this.words.secondWord[this.getRandomNumber(this.words.secondWord.length)] + '-' + this.words.thirdWord[this.getRandomNumber(this.words.thirdWord.length)]
      }
  }
};
</script>

<style scoped lang="scss">
  .flex {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .inline {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 500px;
  }
</style>
