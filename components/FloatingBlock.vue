<template>
<div id="floatingBlock" :class="{threeColumn: iteration === 1, twoRow: iteration === 2}" :style="{background: `hsl(${theme.background.h},${theme.background.s}%,${theme.background.l}%)`}">
  <div v-if="1" id="floatingLeft">
    <slot name="text">

    </slot>
  </div>
  <div v-if="1" id="floatingRight">
    <slot name="image">

    </slot>
  </div>
  <div v-if="2" id="floatingTop">
    <slot name="top">

    </slot>
  </div>
  <div v-if="2" id="floatingBot">
    <slot name="bot">

    </slot>
  </div>
</div>
</template>

<script>
export default {
  name: 'FloatingBlock',
  props:{
    iteration:{
      type: Number,
      default: 1
    },
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
.threeColumn{
  grid-template-columns: 1fr 1fr 1fr;
}
.twoRow{
  grid-template-rows: auto 1fr;
}
#floatingBlock{
  display: grid;
  grid-gap: 1rem;
  width: 70%;
  padding: 3rem;
  border-radius: 30px;
  box-sizing: border-box;
  #floatingLeft{
    grid-column: span 2;
    display: grid;
    align-items: center;
  }
  #floatingRight{
    .score{
    place-self: center;
    width: 80%;
  }
  }
}
</style>
