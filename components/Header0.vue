<template>
<div id="header" :style="styles.darkBackground">
  <slot name="logo">

  </slot>
  <slot name="middle">

  </slot>
  <slot name="numberBlock">

  </slot>
</div>
</template>

<script>
export default {
  name: 'Header0',
  props:{
    theme:{
      type: Object
    },
    styles:{
      type: Object
    }
  }
}
</script>

<style scoped lang="scss">
#header{
  padding: 0.5rem 5% 0.5rem 5%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 0 5px 3px black;
  @media (max-width: 1080px) {
    flex-wrap: wrap;
    justify-content: center;
  }
  .logo{
    width: 22vw;
    @media (max-width: 1080px) {
      width: 100%;
    }
  }
  #middleText{
    @media (max-width: 640px) {
      font-size: 1.45rem;
      margin-bottom: 0;
    }
  }
.number{
  @media (max-width: 640px) {
    font-size: 1.85rem;
  }
}
}
</style>
