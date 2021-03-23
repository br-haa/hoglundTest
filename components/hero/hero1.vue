<template>
  <div id="hero">
    <div id="heroBackgroundHolder">
      <slot name="background"></slot>
    </div>
    <div id="heroText" :style="{background: `linear-gradient(to right, hsl(${hsl.h},${hsl.s}%,${hsl.l}%), hsl(${hsl.h},${hsl.s}%,${hsl.l-20}%))` }">
      <slot name="text">

      </slot>
    </div>
    <div id="hookHolder">
      <slot name="hook"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hero1',
  props:{
    theme:{
      type: Object
    },
  },
    computed: {
     hsl() {
      const {h,s,l} = this.theme.hsla;
      return {h,s,l}
     }
    }
}
</script>

<style scoped lang="scss">
#hero{
  display: grid;
  width: 100%;
  height: 90vh;
  box-sizing: border-box;
  padding: 100px 0 0 0;
  @media (max-width: 1080px) {
    height: 65vh;
  }
  #heroBackgroundHolder{
    z-index: -1;
    grid-area: 1/1/1/1;
    .background{
      width: 100%;
      height: 80vh;
      object-fit: cover;
    }
    @media (max-width: 1080px) {
      height: 65vh;
    }
  }
  #heroText{
    grid-area: 1/1/1/1;
    height: 100%;
    width: 50%;
    justify-self: end;
    padding: 2rem;
    box-sizing: border-box;
    box-shadow: 0 0 5px 3px black;
    display: grid;
    align-items: center;
    #heroTextGroup{
      margin-top: -7rem;
      #blerb {
        max-width: 500px;
      }
    }
    @media (max-width: 1080px) {
      align-items: start;
      align-self: end;
      height: 50%;
      width: 100%;
      #heroTextGroup{
        margin-top: -1rem !important;
      }
      h1{
        font-size: 1.8rem;
      }
    }
  }
  #heroFormHolder{
    grid-area: 1/1/1/1;
    justify-self: end;
    align-self: center;
    width: 22%;
    margin-right: 5%;
    background: black;
    box-sizing: border-box;
    padding: 1rem;
    border-radius: 10px;
    @media (max-width: 1080px) {
      align-self: end;
      width: 100%;
      margin-right: 0;
      justify-self: center;
    }

  }
  #hookHolder{
    grid-area: 1/1/1/1;
    align-self: end;
    justify-self: center;
    margin-bottom: -2rem;
    max-width: 300px;

  }

}
</style>
<style lang="scss">
#form-inside{
  .consent-text{
    font-size: 0.8rem !important;
  }
  .buttonGrid{
    margin-top: .5rem !important;
  }
  #Message{
    height: 100px;
  }
  #formTopText{
    margin: 0;
    @media (max-width: 640px) {
      font-size: 1.5rem;
    }
  }
  #formBotText{
    margin: 0;
    @media (max-width: 640px) {
      font-size: 3rem;
    }
  }
}
</style>
