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
  padding: 0 2rem 0 2rem;
  display: flex;
  justify-content: space-between;
  .logo{
    width: 200px;
  }
}
</style>
