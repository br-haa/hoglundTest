<template>
<div id="header" :style="styles.darkBackground" :class="{ scroll: !atTop}">
  <slot name="logo">

  </slot>
  <slot name="middle" v-if="atTop">

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
    },
    atTop: {
      type: Boolean,
      default: true
    }
  },
 data() {
    return {
    }
  }
}
</script>

<style scoped lang="scss">
#header{
  padding: 0.5rem 5% 0.5rem 5%;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 120px;
  z-index: 600;
  box-shadow: 0 0 5px 3px black;
  width: 100%;
  position: fixed;
  transition: 0.3s;
  @media (max-width: 1080px) {
    flex-wrap: wrap;
    justify-content: center;
    height: 200px;
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
.scroll {
  height: 70px !important;
  background: hsla(217, 20%, 10%, 0.7) !important;
  backdrop-filter: blur(5px);
  @media (max-width: 1080px) {
height: 100px !important;
  }
}
</style>
