<template>
  <div class="contactBlock">
    <slot name="top"></slot>
    <slot name="mid"></slot>
    <slot name="bot"></slot>
  </div>
</template>

<script>
export default {
  name: 'ContactBlock',
}
</script>

<style scoped lang="scss">
.contactBlock {
  width: 40vw;
  margin: 1rem 0 1rem 0;
  @media (max-width: 1080px) {
    width: 100%;
    margin: 1rem 0 1rem 0;
  }
  .contactCallNow {
    font-size: 3.5vw;
    font-weight: bold !important;
    text-align: center;
    @media (max-width: 1080px) {
      font-size: 8vw;
    }
  }
}
</style>
