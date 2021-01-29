<template>
<div id="hero">
  <div id="heroBackgroundHolder">
    <slot name="background"></slot>
  </div>
  <div id="heroText">
    <slot name="text">

    </slot>
  </div>
  <div id="heroFormHolder">
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
  name: 'hero'
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
    grid-area: 1/1/1/1;
    margin-left: 2rem;
    align-self: center;
  }
  #heroFormHolder{
    grid-area: 1/1/1/1;
  }
  #hookHolder{
    grid-area: 1/1/1/1;
   align-self: end;
    justify-self: center;
    margin-bottom: -2rem;

  }
}
</style>
