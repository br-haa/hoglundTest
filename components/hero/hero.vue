<template>
<div id="hero">
  <div id="heroBackgroundHolder">
    <slot name="background"></slot>
  </div>
  <div id="heroText">
    <slot name="text">

    </slot>
  </div>
  <div id="heroFormHolder" :style="{background:`hsl(${this.theme.background.h},${this.theme.background.s}%,${this.theme.background.l}%)`}">
  }">
    <slot name="form">

    </slot>
  </div>
  <div id="hookHolder">
    <slot name="hook"></slot>
  </div>
</div>
</template>

<script>
export default {
  name: 'hero',
  props:{
    theme:{
      type: Object
    }
  }
}
</script>

<style scoped lang="scss">
#hero{
  display: grid;
  width: 100%;
  height: 80vh;
  box-sizing: border-box;
@media (max-width: 1080px) {
  height: 150vh;
}
  #heroBackgroundHolder{
    z-index: -1;
  grid-area: 1/1/1/1;
    .background{
      width: 100%;
      height: 80vh;
      object-fit: cover;
    }
  }
  #heroText{
    grid-area: 1/1/1/1;
    margin-left: 5%;
    align-self: center;
    @media (max-width: 1080px) {
      align-self: start;
      margin: 0 5% 0 5%;
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
      width: 90%;
      margin-right: 0;
      justify-self: center;
    }

  }
  #hookHolder{
    grid-area: 1/1/1/1;
   align-self: end;
    justify-self: center;
    margin-bottom: -2rem;
    @media (max-width: 1080px) {
      align-self: center;
    }
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
}
</style>
