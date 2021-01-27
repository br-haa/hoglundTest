<template>
  <div>
    <Nuxt />
 <Header0 :theme="themes.dark">
   <template v-slot:logo>
     <img :src="displayPic('logoWhite.svg')" alt="logo">
   </template>
   <template v-slot:middle>
    <h3>Free Immediate Case Evaluation</h3>
   </template>
   <template v-slot:numberBlock>
   </template>
 </Header0>
    <hero :theme="themes.dark">
      <template v-slot:background></template>
      <template v-slot:text>
        <div>
          <h1>$0 Down Bankruptcy ™*</h1>
          <h3>File Now - Pay Attorney Fees Later</h3>
          <p>Free Confidential Phone Consultation With An
            Experienced Bankruptcy Attorney
          </p>
        </div>
      </template>
      <template v-slot:form></template>
      <template v-slot:hook>
        <DynamicButton :style="customStyles">Why Hoglund Law?<br>Click Here To Find Out</DynamicButton>
      </template>
    </hero>
    <div class="lightWrapper">
    <FloatingBlock :theme="themes.dark" :style="customStyles">
      <template v-slot:text>
        <div>
          <h2>Minnesota’s Largest
            Bankruptcy Law Firm</h2>
          <p>
            70+ Years Of Combined Experience
            Over 47,000 Clients Trusted Us
          </p>
        </div>
      </template>
      <template v-slot:image>
        <img :src="displayPic('720.svg')" alt="720">
      </template>
    </FloatingBlock>
    <Scroller :theme="themes.light" :style="customStyles">
      <template v-slot:title>
        <h3>Why Hoglund Law?</h3>
      </template>
    </Scroller>
    </div>
    <div class="darkWrapper" :style="customStyles.darkBackground">
      <div>
        <div>
          <h3>One Of Minnesota's Most
            Experienced Bankruptcy Law Firms</h3>
          <P>70+ Years Of Combined Bankruptcy Experience</P>
        </div>
        <div class="whiteLine"></div>
        <ReviewBlock :theme="themes.dark" :style="customStyles">
          <template v-slot:left>
            <img :src="displayPic('googleLogo.svg')" alt="google logo">
          </template>
          <template v-slot:mid>
            <div>
              <h4>220+ Google Reviews</h4>
              <div id="starsHolder">
                <img v-for="(star,index) in 4" :key="index" :src="displayPic('star.svg')" alt="star">
                <img :src="displayPic('starHalf.svg')" alt="star">
              </div>
            </div>
          </template>
          <template v-slot:right>
            <DynamicButton :theme="themes.dark" :style="customStyles" >Read More</DynamicButton>
          </template>
        </ReviewBlock>
      </div>
    </div>
    <div class="lightWrapper" :style="customStyles.lightBackground">
      <ContactBlock :theme="themes.light" :style="customStyles">
        <template v-slot:top>
          <img :src="displayPic('logoBlue.svg')" alt="logo">
        </template>
        <template v-slot:mid></template>
        <template v-slot:bot>
          <DynamicButton :theme="themes.light" :style="customStyles">Or Message Us</DynamicButton>
        </template>
      </ContactBlock>
      <FloatingBlock :theme="themes.dark" :style="customStyles"></FloatingBlock>
      <div>
        <h4>The Call Is FREE! The Evaluation Is FREE!</h4>
        <h2>We Can Help!</h2>
      </div>
    </div>
    <div class="darkWrapper" :style="[customStyles.darkBackground, customStyles.darkText]">
      <Testimonials :theme="themes.dark" :style="customStyles"></Testimonials>
      <div>
        <div class="accentLine"></div>
        <ContactBlock :theme="themes.dark" :style="customStyles">
          <template v-slot:top>
            <img :src="displayPic('logoWhite.svg')" alt="logo">
          </template>
          <template v-slot:mid></template>
          <template v-slot:bot>
            <DynamicButton :theme="themes.dark" :style="customStyles">Or Message Us</DynamicButton>
          </template>
        </ContactBlock>
        <div class="accentLine"></div>
      </div>
      <DisclaimerAndCopyright :theme="themes.dark" :style="customStyles"></DisclaimerAndCopyright>
    </div>
  </div>
</template>
<style>
</style>
<script>
import Header0 from '../components/Header0'
import Hero from '../components/hero/hero'
import FloatingBlock from '../components/FloatingBlock'
import Scroller from '../components/Scroller'
import ReviewBlock from '../components/ReviewBlock'
import ContactBlock from '../components/ContactBlock'
import Testimonials from '../components/Testimonials'
import DisclaimerAndCopyright from '../components/DisclaimerAndCopyright'
import DynamicButton from '../components/DynamicButton'
export default {
  components: { DynamicButton, DisclaimerAndCopyright, Testimonials, ContactBlock, ReviewBlock, Scroller, FloatingBlock, Hero, Header0 },
  data(){
    return{
      themes:{
        light:{
          hsla:{h:217,s:73,l:15,a:1},
          accent:{h:197, s:100, l:46, a:1},
          background:{h:197, s:10, l:100, a:1},
          textColor:{h:217, s:87, l:6, a:1},
          isDark:false,
        },
        dark:{
          hsla:{h:217,s:73,l:15,a:1},
          accent:{h:43,s:93,l:52,a:1},
          background:{h:217, s:87, l:6, a:1},
          textColor:{h:217, s:87, l:100, a:1},
          isDark:false,
        }
      }
    }
  },
  computed:{
    customStyles(){
      return {
        lightBackground: {
          background: `hsl(${this.themes.light.background.h},${this.themes.light.background.s}%,${this.themes.light.background.l}%)`,
          color: `hsl(${this.themes.light.textColor.h},${this.themes.light.textColor.s}%,${this.themes.light.textColor.l}%)`
        },
        lightText: {color: `hsl(${this.themes.light.textColor.h},${this.themes.light.textColor.s}%,${this.themes.light.textColor.l}%)`},
        lightAccentBg: {background: `hsl(${this.themes.light.accent.h},${this.themes.light.accent.s}%,${this.themes.light.accent.l}%)` },
        lightAccentText: {color: `hsl(${this.themes.light.accent.h},${this.themes.light.accent.s}%,${this.themes.light.accent.l}%)` },
        darkBackground: {
          background: `hsl(${this.themes.dark.background.h},${this.themes.dark.background.s}%,${this.themes.dark.background.l}%)`,
          color: `hsl(${this.themes.dark.textColor.h},${this.themes.dark.textColor.s}%,${this.themes.dark.textColor.l}%)`
        },
        darkText: {color: `hsl(${this.themes.dark.textColor.h},${this.themes.dark.textColor.s}%,${this.themes.dark.textColor.l}%)`},
        darkAccentBg: {background: `hsl(${this.themes.dark.accent.h},${this.themes.dark.accent.s}%,${this.themes.dark.accent.l}%)` },
        darkAccentText: {color: `hsl(${this.themes.dark.accent.h},${this.themes.dark.accent.s}%,${this.themes.dark.accent.l}%)` }
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
