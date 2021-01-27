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

<style scoped>

</style>
