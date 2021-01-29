<template>
<div class="contactBlock">
  <slot name="top"></slot>
  <slot name="mid"></slot>
  <slot name="bot"></slot>
</div>
</template>

<script>
export default {
  name: 'ContactBlock'
}
</script>

<style scoped lang="scss">
.contactBlock{
  width: 40%;
  margin: 3rem 0 3rem 0;
}
</style>
