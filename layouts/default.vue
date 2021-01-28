<template>
  <div>
    <Nuxt />
 <Header0 :theme="themes.dark" :styles="customStyles">
   <template v-slot:logo>
     <img class="logo" :src="displayPic('logoWhite.svg')" alt="logo">
   </template>
   <template v-slot:middle>
    <h3>Free Immediate Case Evaluation</h3>
   </template>
   <template v-slot:numberBlock>
     <div>
       <h4>Call Now 123-456-7890</h4>
       <DynamicButton :theme="themes.dark">Get Started Today!</DynamicButton>
     </div>
   </template>
 </Header0>

    <hero :theme="themes.dark">
      <template v-slot:background>
        <img class="background" :src="displayPic('backgrounds/bg.png')" alt="background">
      </template>
      <template v-slot:text>
        <div>
          <h1 :style="customStyles.darkAccentText">$0 Down Bankruptcy ™*</h1>
          <h3 :style="customStyles.darkText">File Now - Pay Attorney Fees Later</h3>
          <p :style="customStyles.darkAccentText">Free Confidential Phone Consultation With An
            Experienced Bankruptcy Attorney
          </p>
        </div>
      </template>
      <template v-slot:form></template>
      <template v-slot:hook>
        <DynamicButton :theme="themes.dark">Why Hoglund Law?<br>Click Here To Find Out</DynamicButton>
      </template>
    </hero>

    <div class="lightWrapper">
    <div class="topFloaterSpacer">
     <FloatingBlock :theme="themes.dark" :styles="customStyles">
      <template v-slot:text>
        <div>
          <h2 :style="customStyles.darkText">Minnesota’s Largest
            Bankruptcy Law Firm</h2>
          <p :style="customStyles.darkAccentText">
            70+ Years Of Combined Experience
            Over 47,000 Clients Trusted Us
          </p>
        </div>
      </template>
      <template v-slot:image>
        <img class="score" :src="displayPic('720.svg')" alt="720">
      </template>
    </FloatingBlock>
    </div>
      <div class="scrollerSpacer">
    <Scroller :theme="themes.light" :style="customStyles">
      <template v-slot:title>
        <h3>Why Hoglund Law?</h3>
      </template>
    </Scroller>
      </div>
    </div>

    <div class="darkWrapper experiencedWrapper" :style="customStyles.darkBackground">
      <div id="experiencedHolder">
        <div>
          <h3 :style="customStyles.darkText">One Of Minnesota's Most<br>
            Experienced Bankruptcy Law Firms</h3>
          <P :style="customStyles.darkAccentText">70+ Years Of Combined Bankruptcy Experience</P>
        </div>
        <div class="whiteLine"></div>
        <div id="reviewBlockHolder">
          <ReviewBlock :theme="themes.dark" :style="customStyles">
            <template v-slot:left>
              <img :src="displayPic('googleLogo.svg')" alt="google logo">
            </template>
            <template v-slot:mid>
              <div>
                <h4>220+ Google Reviews</h4>
                <div class="starsHolder">
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
    </div>

    <div class="lightWrapper" :style="customStyles.lightBackground">
      <div class="contactBlockHolder">
        <ContactBlock :theme="themes.light" :style="customStyles">
          <template v-slot:top>
            <img :src="displayPic('logoBlue.svg')" alt="logo">
          </template>
          <template v-slot:mid></template>
          <template v-slot:bot>
            <DynamicButton :theme="themes.light">Or Message Us</DynamicButton>
          </template>
        </ContactBlock>
      </div>

      <div class="botFloaterSpacer">
        <FloatingBlock :iteration="2" :theme="themes.dark" :style="customStyles">
          <template v-slot:top>
            <div>
              <h2 :style="customStyles.darkAccentText">
                Get A Fresh Start?
              </h2>
              <h3 :style="customStyles.darkText">
                Most clients are able to...
              </h3>
            </div>
          </template>
          <template v-slot:bot>
          <ul :style="customStyles.darkText">
            <li>
              Stop collection harassment.
            </li>
            <li>
              Stop wage garnishment.
            </li>
            <li>
              Stop home foreclosure.
            </li>
            <li>
              Prevent auto repossession.
            </li>
            <li>
              Lower their monthly payments.
            </li>
          </ul>
          </template>
        </FloatingBlock>
      </div>

      <div class="botCta">
        <h4>The Call Is FREE! The Evaluation Is FREE!</h4>
        <h2 :style="customStyles.lightAccentText">We Can Help!</h2>
      </div>
    </div>

    <div class="darkWrapper" :style="[customStyles.darkBackground, customStyles.darkText]">
      <Testimonials :theme="themes.dark" :style="customStyles"></Testimonials>
      <div>
        <div class="accentLine" :style="customStyles.darkAccentBg"></div>
        <div class="contactBlockHolder">
        <ContactBlock :theme="themes.dark" :style="customStyles">
          <template v-slot:top>
            <img :src="displayPic('logoWhite.svg')" alt="logo">
          </template>
          <template v-slot:mid></template>
          <template v-slot:bot>
            <DynamicButton :theme="themes.dark" :style="customStyles">Or Message Us</DynamicButton>
          </template>
        </ContactBlock>
        </div>
        <div class="accentLine" :style="customStyles.darkAccentBg"></div>
      </div>
      <DisclaimerAndCopyright :theme="themes.dark" :style="customStyles"></DisclaimerAndCopyright>
    </div>

  </div>
</template>

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

<style scoped lang="scss">
.topFloaterSpacer{
  display: grid;
  place-items: center;
  margin: 6rem 0 3rem 0;
}
.experiencedWrapper{
  display: grid;

  #experiencedHolder{
    display: grid;
    place-items: center;
    padding: 3rem;
    height: 30rem;
  }
  .whiteLine{
    height: 3px;
    width: 80%;
    background: white;
  }
  #reviewBlockHolder{
    display: grid;
    place-items: center;
  }
}

.botFloaterSpacer{
  display: grid;
  place-items: center;
  margin: 6rem 0 3rem 0;
}
.contactBlockHolder{
  display:grid;
  place-items: center;
}
.darkWrapper{
  padding: 0 2rem 0 2rem;
}
.lightWrapper{
  padding: 0 2rem 0 2rem;
}
.accentLine{
  height: 3px;
  width: 100%;
}
</style>
