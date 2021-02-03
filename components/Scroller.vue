<template>
<div id="scroller">

  <div>
    <div id="titleGrid">
      <div class="titleLine" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}"></div>
      <slot name="title"></slot>
      <div class="titleLine" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}"></div>
    </div>
    <div id="scrollerHolder">
      <button class="scrollButton" id="leftButton" @click="move('back')">
      <span class="buttonArrow" :style="{background:`hsl(${theme.accent.h},${theme.accent.s}%,${theme.accent.l}%)`}">

      </span>
      </button>
      <div class="textDisplay">
        <transition name="slide" mode="out-in">
          <h2 :key="items[counter]">{{items[counter]}}</h2>
        </transition>
      </div>
      <button class="scrollButton" id="rightButton" @click="move('front')">
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
  data(){
return{
  counter: 0,
  items: [
    'Free Confidential Consultations',
    'Free 720 Program',
    'Free E-Book On Bankruptcy',
    'Affordable Payment Plans',
    'Over 47,000 Clients Trusted Us',
    '70+ Years Of Combined Experience',
    'Chapter 7, 13 & Business Bankruptcy',
    'Call Days, Evenings, Or Weekends',
  ]
}
  },
  props:{
    theme:{
      type: Object
    }
  },
  methods:{
    move(direction){
      if(direction === 'back'){
        if(this.counter === 0){
          this.counter = this.items.length - 1
        } else{
          this.counter --
        }
      } else {
        if(this.counter === this.items.length - 1){
          this.counter = 0
        } else{
          this.counter ++
        }
      }
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
  transition: .3s;
  &:focus {
    outline: none;
  }
  &:active{
    transition: 0.01s !important;
    transform: scale(0.99) !important;
    filter: drop-shadow(0 0 1px black) !important;
  }
  &:hover{
    transform: scale(1.1);
    filter: drop-shadow(0 0 5px black);
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
  margin-bottom: 1rem;
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

.slide-enter-active {
  animation: fade 0.5s forwards;
}
.slide-enter{
  opacity: 0;
}
.slide-leave-to {
  animation: fade 0.5s reverse;
}
@keyframes fade {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
