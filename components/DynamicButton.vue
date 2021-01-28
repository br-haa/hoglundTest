<template>
<button :style="{background: `hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}" @click="$emit('buttonClick')">
<slot></slot>
</button>
</template>

<script>
export default {
  name: 'dynamicButton',
  props:{
    theme:{
      type: Object
    }
  }
}
</script>

<style scoped lang="scss">
button{
  border-radius: 360px;
  padding: .5rem 3rem .5rem 3rem;
  width: 100%;
  border: none;
  cursor: pointer;
  box-shadow: 0 0 5px 3px black;
  &:focus{
    outline: none;
  }
}
</style>
