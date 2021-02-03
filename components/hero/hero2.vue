<template>
  <div id="hero">
    <div id="heroBackgroundHolder">
      <slot name="background"></slot>
    </div>
    <div id="heroText">
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
  name: 'hero2',
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
    display: grid;
    justify-self: center;
    grid-area: 1/1/1/1;
    align-self: center;
    text-align: center;
    margin-top: -7rem;
    #headline{
      margin: 0;
    }
    #subHead{
      margin: 0;
    }
    #blerb{
      margin: 2rem 0 0 0;
    }
    @media (max-width: 1080px) {
      align-self: center;
      margin: -7rem 5% 0 5%;
      text-align: left;
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
