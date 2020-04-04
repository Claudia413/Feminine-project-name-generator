<template>
  <div class="flex">
    <h1>A feminine project name generator</h1>
    <div class="inline">
      <div class="relative">
        <input class="name" id="generated-name" v-model="name" @click="copyTextToClipboard()"/>
        <p :class="name === ''? 'instructions hidden' : 'instructions'">Click on the name to copy it</p>
        </div>
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
      },
      copyTextToClipboard() {
        var name = document.getElementById('generated-name')
        name.focus();
        name.select();
        document.execCommand("copy");
      }
  }
};
</script>

<style scoped lang="scss">
  h1 {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 42px;
    line-height: 71px;
    margin-bottom: 96px;
  }
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
    width: 600px;
    @media screen and (max-width: 768px) {
      flex-direction: column-reverse;
      width: 100%;
    }
  }
  .name {
    border: none;
    color: inherit;
    font-family: 'Raleway', sans-serif;
    padding: 20px;
    background: #fff5f2;
    width: 400px;
    height: 61px;
    box-sizing: border-box;
    border-radius: 24px;
    font-size: 18px;
    font-weight: bold;
    box-shadow: inset 8px 8px 16px #d9d0ce,
                inset -8px -8px 16px #fcf9f9;
    &:focus {
      outline: none;
    }
    &::selection {
      background: #2a4c6d;
      color: #fcf9f9;
    }
  }
  .relative {
    position: relative;
    margin: 50px 0;
  }
  .instructions {
    position: absolute;
    left: 126px;
    color: #bcbcbc;
    font-size: 12px;
    transition: all 0.4s ease-in;
    &.hidden {
      opacity: 0;
    }

  }
</style>
