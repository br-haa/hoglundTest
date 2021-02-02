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
  display: flex;
  align-items: center;
 justify-self: center;
  grid-gap: 1rem;
  @media (max-width: 1080px) {
    flex-wrap: wrap;
  }

}
#left{
  width: 100px;
}
#mid{
  display: grid;
  place-items: center;
  height: 100%;
  h4,h5,h3,h2,h1{
    margin: 0;
    white-space: nowrap;
  }
}
.starsHolder{
  display: flex;
  width: 98%;
  justify-content: space-between;
  img{
    width: 40px;
    height: 40px;
  }
}
</style>
