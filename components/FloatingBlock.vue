<template>
<div id="floatingBlock" :class="{threeColumn: iteration === 1, twoRow: iteration === 2}" :style="background.darkTexture">
  <div v-if="iteration === 1" id="floatingLeft">
    <slot name="text">

    </slot>
  </div>
  <div v-if=" iteration === 1" id="floatingRight">
    <slot name="image">

    </slot>
  </div>
  <div v-if="iteration === 2" id="floatingTop">
    <slot name="top">

    </slot>
  </div>
  <div v-if="iteration === 2" id="floatingBot">
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
  },
  computed:{
    background(){
      return {
        darkTexture: {
          background: `hsl(${this.theme.background.h},${this.theme.background.s}%,${this.theme.background.l}%) url(${this.displayPic('backgrounds/lines.svg')})`,
          backgroundSize:'200% auto, 100% auto',
          backgroundPosition: 'center',
          color: `hsl(${this.theme.textColor.h},${this.theme.textColor.s}%,${this.theme.textColor.l}%)`
        },
      }
    }
  },
  methods:{
    displayPic(pic) {
      return require(`@/assets/img/${pic}`);
    },
  }
}
</script>

<style scoped lang="scss">
.threeColumn{
  grid-template-columns: 1fr 1fr 1fr;
  @media  (max-width: 1080px){
    grid-template-columns: 1fr;
  }
}
.twoRow{
  grid-template-rows: auto 1fr;
  grid-template-columns: 1fr;

}
#floatingBlock{
  display: grid;
  grid-gap: 1rem;
  width: 80%;
  padding: 3rem 5% 3rem 5%;
  border-radius: 30px;
  box-sizing: border-box;
  box-shadow: 0 0 5px 3px black;
  @media (max-width: 1080px) {
    width: 98%;
  }
  #floatingLeft{
    grid-column: span 2;
    display: grid;
    align-items: center;
    @media  (max-width: 1080px){
      grid-column: span 1;
    }
  }
  #floatingRight{
    .score{
    place-self: center;
    width: 80%;
  }
  }
}
</style>
