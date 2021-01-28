<template>
<div class="reviewBlock">
  <div id="left">
    <slot name="left"></slot>
  </div>
<div id="mid">
  <slot name="mid"></slot>
</div>
<div id="right">
  <slot name="right"></slot>
</div>
</div>
</template>

<script>
export default {
name: "ReviewBlock"
}
</script>

<style scoped lang="scss">
.reviewBlock{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
 justify-self: center;
}
#left{
  width: 100px;
}
#mid{
  grid-column: span 3;
}
.starsHolder{
  display: flex;
  width: 100%;
  justify-content: space-between;
  img{
    width: 20px;
    height: 20px;
  }
}
</style>
