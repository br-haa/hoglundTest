<template>
<div id="scroller">
  <div id="titleGrid">
    <div class="titleLine"></div>
    <slot name="title"></slot>
    <div class="titleLine"></div>
  </div>
  <div>
    <h3 id="cts">Click To Scroll</h3>
    <div class="scrollerLine"></div>
    <div id="scrollerHolder">
      <button>L</button>
      <div class="textDisplay">
        <h2>example text</h2>
      </div>
      <button>R</button>
    </div>
    <div class="scrollerLine"></div>
  </div>

</div>
</template>

<script>
export default {
  name: 'Scroller'
}
</script>

<style scoped lang="scss">
#titleGrid{
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  grid-gap: 1rem;
  .titleLine{
    height: 3px;
    width: 100%;
    background: black;
  }
}
#scroller{
  margin: 1rem auto 6rem auto;
  width: 70%;
  box-sizing: border-box;
}
#scrollerHolder{
  display: flex;
  justify-content: space-between;
}
.scrollerLine{
  width: 80%;
  height: 3px;
  background: black;
  margin: auto;
}
.textDisplay{
  text-align: center;
}
#cts{
  text-align: center;
  margin-bottom: 5px;
}
</style>
