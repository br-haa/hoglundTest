<template>
<div id="scroller">
  <div id="titleGrid">
    <div class="titleLine" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}"></div>
    <slot name="title"></slot>
    <div class="titleLine" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}"></div>
  </div>
  <div>
    <p id="cts">Click To Scroll</p>
    <div class="scrollerLine" :style="{background:`hsl(${theme.textColor.h},${theme.textColor.s}%,${theme.textColor.l}%)`}"></div>
    <div id="scrollerHolder">
      <button class="scrollButton" id="leftButton">
      <span class="buttonArrow" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}">

      </span>
      </button>
      <div class="textDisplay">
        <h2>No Fee If No Recovery</h2>
      </div>
      <button class="scrollButton" id="rightButton">
              <span class="buttonArrow" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}">
      </span>
      </button>
    </div>
    <div class="scrollerLine"></div>
  </div>

</div>
</template>

<script>
export default {
  name: 'Scroller',
  props:{
    theme:{
      type: Object
    }
  }
}
</script>

<style scoped lang="scss">
.scrollButton{
  border: none;
  height: 100px;
  width: 100px;
  cursor: pointer;
  background: none;
  filter: drop-shadow(0 0 3px black);
  &:focus{
    outline: none;
  }
  @media (max-width: 1080px) {
    height: 60px;
    width: 60px;
  }
  .buttonArrow{
    display: block;
    clip-path: polygon(75% 0%, 100% 50%, 77% 100%, 37% 100%, 63% 51%, 40% 0);
    height: 100%;
    width: 100%;
    user-focus: none;
    pointer-events: none;
  }
}
#leftButton{
  .buttonArrow{
    transform: rotate(180deg);
  }

}
#titleGrid{
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  grid-gap: 1rem;
  margin-bottom: 3rem;
  @media (max-width: 1080px) {
    margin-bottom: 1rem;
  }
  .titleLine{
    height: 3px;
    width: 70%;
    background: black;
    &:first-child{
      justify-self: end;
    }
  }
}
#scroller{
  box-sizing: border-box;
}
#scrollerHolder{
  display: flex;
  justify-content: space-between;
}
.scrollerLine{
  width: 80%;
  height: 3px;
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
