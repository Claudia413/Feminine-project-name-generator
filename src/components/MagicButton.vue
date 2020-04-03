<template>
    <div class="button" @click="$emit('generate')"><span>Generate</span></div>
</template>

<script>

export default {
  name: 'MagicButton',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .button {
      display: flex;
      justify-content: center;
      align-items: center;
      border: none;
      width: 150px;
      height: 80px;
      border-radius: 28px;
      background: #fff5f2;
      box-shadow:  8px 8px 16px #d9d0ce,
                  -8px -8px 16px #fcf9f9;
      font-family: 'Raleway', sans-serif;
      span {
        display: block;
        font-size: 18px;
        font-weight: bold;
        background: -webkit-linear-gradient(left top, #FEDB37, #FDB931, #9f7928, #8A6E2F);
        background: -webkit-linear-gradient(left top, #a66251, #fcc1b9, #ac6d5d, #ffd2d2);
        // background: -webkit-linear-gradient(left top, #ac6943, #fbd1c1, #ab6943, #faf4ed);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
      }
      &:active {
        border-radius: 28px;
        background: #fff5f2;
        box-shadow: inset 8px 8px 16px #d9d0ce,
                    inset -8px -8px 16px #fcf9f9;
        span {
          position: relative;
          top: 1px;
        }
      }
      &:focus {
        outline: none;
      }
  }
</style>
