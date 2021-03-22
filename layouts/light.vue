
<template>
  <div>
    <Nuxt />
    <Header0 :theme="$store.state.themes.dark" :styles="customStyles">
      <template v-slot:logo>
        <img class="logo" :src="displayPic('logoWhite.svg')" alt="logo">
      </template>
      <template v-slot:middle>
        <h3 id="middleText" class="thinText">Free Immediate Case Evaluation</h3>
      </template>
      <template v-slot:numberBlock>
        <div>
          <h4 class="number">Call Now <span :style="customStyles.darkAccentText">123-456-7890</span></h4>
          <DynamicButton :theme="$store.state.themes.dark">Get Started Today!</DynamicButton>
        </div>
      </template>
    </Header0>

  <hero1 :theme="$store.state.themes.light">
    <template v-slot:background>
      <img class="background" :src="displayPic('backgrounds/city.png')" alt="background">
    </template>
    <template v-slot:text>
      <div id="heroTextGroup">
        <h2 id="headline" :style="customStyles.darkAccentText">$0 Down Bankruptcy ™*</h2>
        <h3 id="subHead" :style="customStyles.darkText">File Now - Pay Attorney Fees Later</h3>
        <h5 id="blerb" :style="customStyles.darkAccentText">Free Confidential Phone Consultation<br>With An
          Experienced Bankruptcy Attorney
        </h5>
      </div>
    </template>
    <template v-slot:hook>
      <DynamicButton :theme="$store.state.themes.dark">Why Hoglund Law?<br>Click Here To Find Out</DynamicButton>
    </template>
  </hero1>
<div id="formBlock" :style="customStyles.darkTexture">
  <form-controller :theme="$store.state.themes.dark">
    <h3 id="formTopText" :style="customStyles.darkText">No Office Visit Necessary</h3>
    <h2 id="formBotText" :style="customStyles.darkAccentText">Tag Line</h2>
  </form-controller>
</div>
    <div class="lightWrapper" :style="customStyles.lightBackground">
      <div class="topFloaterSpacer">
        <FloatingBlock :theme="$store.state.themes.dark" :styles="customStyles">
          <template v-slot:text>
            <div>
              <h2 :style="customStyles.darkText">Minnesota’s Largest
                Bankruptcy Law Firm</h2>
              <h5 :style="customStyles.darkAccentText">
                70+ Years Of Combined Experience<br>
                Over 47,000 Clients Trusted Us
              </h5>
            </div>
          </template>
          <template v-slot:image>
            <img class="score" :src="displayPic('720.svg')" alt="720">
          </template>
        </FloatingBlock>
      </div>
      <div class="scrollerSpacer">
        <Scroller :theme="$store.state.themes.light" :style="customStyles">
          <template v-slot:title>
            <h3>Why Hoglund Law?</h3>
          </template>
        </Scroller>
      </div>
    </div>

    <div class="darkWrapper experiencedWrapper" :style="customStyles.darkTexture">
      <div id="experiencedHolder">
        <div>
          <h3 :style="customStyles.darkText">One Of Minnesota's Most<br>
            Experienced Bankruptcy Law Firms</h3>
          <h4 :style="customStyles.darkAccentText">70+ Years Of Combined Bankruptcy Experience</h4>
        </div>
        <div class="whiteLine"></div>
        <div id="reviewBlockHolder">
          <ReviewBlock :theme="$store.state.themes.dark" :style="customStyles">
            <template v-slot:left>
              <img :src="displayPic('googleLogo.svg')" alt="google logo">
            </template>
            <template v-slot:mid>
              <div>
                <h3>220+ Google Reviews</h3>
                <div class="starsHolder">
                  <img v-for="(star,index) in 4" :key="index" :src="displayPic('star.svg')" alt="star">
                  <img :src="displayPic('starHalf.svg')" alt="star">
                </div>
              </div>
            </template>
            <template v-slot:right>
              <DynamicButton :theme="$store.state.themes.dark" :style="customStyles" >Read More</DynamicButton>
            </template>
          </ReviewBlock>
        </div>
      </div>
    </div>

    <div class="lightWrapper" :style="customStyles.lightBackground">
      <div class="contactBlockHolder">
        <ContactBlock :theme="$store.state.themes.light" :style="customStyles">
          <template v-slot:top>
            <img :src="displayPic('logoBlue.svg')" alt="logo">
          </template>
          <template v-slot:mid>
            <h3 class="contactCallNow">Call Now <span :style="customStyles.lightAccentText">123-456-7890</span></h3>
          </template>
          <template v-slot:bot>
            <DynamicButton :theme="$store.state.themes.light">Or Message Us</DynamicButton>
          </template>
        </ContactBlock>

      </div>

      <div class="botFloaterSpacer">
        <FloatingBlock :iteration="2" :theme="$store.state.themes.dark" :style="customStyles">
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
            <div id="freshListHolder">
              <ul :style="customStyles.darkText">
                <li>
                  Stop collection harassment.
                </li>
                <li>
                  Stop wage garnishment.
                </li>
              </ul>
              <ul :style="customStyles.darkText">
                <li>
                  Stop home foreclosure.
                </li>
                <li>
                  Prevent auto repossession.
                </li>
              </ul>
              <ul :style="customStyles.darkText">
                <li>
                  Lower their monthly payments.
                </li>
              </ul>
            </div>
          </template>
        </FloatingBlock>
      </div>

      <div id="botCta">
        <h3>The Call Is FREE! <br class="showAtSmall"> The Evaluation Is FREE!</h3>
        <h2 :style="customStyles.lightAccentText">We Can Help!</h2>
      </div>
    </div>

    <div class="darkWrapper" :style="[customStyles.darkTexture, customStyles.darkText]">
      <Testimonials :theme="$store.state.themes.dark" :style="customStyles"></Testimonials>
      <div>
        <div class="accentLine" :style="customStyles.darkAccentBg"></div>
        <div class="contactBlockHolderBottom">
          <ContactBlock :theme="$store.state.themes.dark" :style="customStyles">
            <template v-slot:top>
              <img :src="displayPic('logoWhite.svg')" alt="logo">
            </template>
            <template v-slot:mid>
              <h3 class="contactCallNow">Call Now <span :style="customStyles.darkAccentText">123-456-7890</span></h3>
            </template>
            <template v-slot:bot>
              <DynamicButton :theme="$store.state.themes.dark" :style="customStyles">Or Message Us</DynamicButton>
            </template>
          </ContactBlock>
        </div>
        <div class="accentLine" :style="customStyles.darkAccentBg"></div>
      </div>
      <DisclaimerAndCopyright :theme="$store.state.themes.dark" :style="customStyles"></DisclaimerAndCopyright>
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
import Hero1 from '../components/hero/hero1'
export default {
  components: { Hero1, DynamicButton, DisclaimerAndCopyright, Testimonials, ContactBlock, ReviewBlock, Scroller, FloatingBlock, Hero, Header0 },
  data(){
    return{
    }
  },
  computed:{
    customStyles(){
      const {h:dh, s:ds, l:dl, a:da} = this.$store.state.themes.dark.hsla;
      const {h:dth,s:dts,l:dtl,a:dta} = this.$store.state.themes.dark.textColor;
      const {h:dah,s:das,l:dal,a:daa} = this.$store.state.themes.dark.accent;
      const {h:dbh,s:dbs,l:dbl,a:dba} = this.$store.state.themes.dark.background;
      const {h:lh,s:ls,l:ll,a:la} = this.$store.state.themes.light.hsla;
      const {h:lth,s:lts,l:ltl,a:lta} = this.$store.state.themes.light.textColor;
      const {h:lah,s:las,l:lal,a:laa} = this.$store.state.themes.light.accent;
      const {h:lbh,s:lbs,l:lbl,a:lba} = this.$store.state.themes.light.background;
      return {
        lightBackground: {
          background: `hsl(${lbh},${lbs}%,${lbl}%) url(${this.displayPic('backgrounds/bgWhite.svg')})`,
          backgroundSize:'cover, 100% auto',
          color: `hsl(${lth},${lts}%,${ltl}%`
        },
        lightText: {color: `hsl(${lth},${lts}%,${ltl}%`},
        lightAccentBg: {background: `hsl(${lah},${las}%,${lal}%)` },
        lightAccentText: {color: `hsl(${lah},${las}%,${lal}%)` },
        darkBackground: {
          background: `hsl(${dbh},${dbs}%,${dbl}%)`,
          color: `hsl(${dth},${dts}%,${dtl}%)`
        },
        darkTexture: {
          background: `hsl(${dh}, ${ds}%, ${dl}%) url(${this.displayPic('backgrounds/lines.svg')})`,
          backgroundSize:'200% auto, 100% auto',
          backgroundPosition: 'center',
          color: `hsl(${dth},${dts}%,${dtl}%)`
        },
        darkText: {color: `hsl(${dth},${dts}%,${dtl}%)`},
        darkAccentBg: {background: `hsl(${dah},${das}%,${dal}%)` },
        darkAccentText: {color: `hsl(${dah},${das}%,${dal}%)` },
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

#formBlock{
  padding: 5rem 10% 4rem 10%;
}

.showAtSmall{
  display: none;
  @media (max-width: 640px) {
    display: initial;
  }
}
.hideAtSmall{
  @media (max-width: 640px) {
    display: none;
  }
}
.thinText{
  font-weight: 200;
}
.topFloaterSpacer{
  display: grid;
  place-items: center;
}
.experiencedWrapper{
  display: grid;

  #experiencedHolder{
    display: grid;
    place-items: center;
    padding: 3rem;
    height: 30rem;
    @media (max-width: 1080px) {
      padding: 0;
    }
  }
  .whiteLine{
    height: 3px;
    width: 70%;
    background: white;
    @media (max-width: 1080px) {
      width: 100%;
    }
  }
  #reviewBlockHolder{
    display: grid;
    width: 70%;
    place-items: center;
    @media (max-width: 1080px) {
      width: 90%;
    }
  }
}

.scrollerSpacer{
  justify-self: center;
  width: 80%;
  margin-top: 3rem;
  @media (max-width: 1080px) {
    width: 100%;
  }
}

#freshListHolder{
  display: flex;
  grid-gap: 2rem;
  flex-wrap: wrap;
  li{
    font-size:clamp(1.1rem, 10 * 1vw / 2.6, 1.85rem) ;
    &::marker{
      color: hsl(43, 93%, 52%);
      content:'✔ '
    }
  }
  @media (max-width: 1080px) {
    grid-gap: 0;
    ul{
      margin: 0;
      padding-left: 6%;
      li{
        &:first-child{
          margin-top: 0;
        }
      }
    }
  }
}
.botFloaterSpacer{
  display: grid;
  place-items: center;
}
#botCta{
  text-align: center;
  margin: 3rem 0 0 0;
  @media (max-width: 1080px) {
    margin: 1rem 0 1rem 0;
  }
}
.contactBlockHolder{
  display:grid;
  place-items: center;
  margin: 0 0 3rem 0;
  @media (max-width: 1080px) {
    margin: 1rem 0 1rem 0;
  }
}
.contactBlockHolderBottom{
  display:grid;
  place-items: center;
  margin: 3rem 0 3rem 0;
  @media (max-width: 1080px) {
    margin: 1rem 0 1rem 0;
  }
}
.darkWrapper{
  padding: 0 5% 0 5%;
}
.lightWrapper{
  padding: 4rem 5% 4rem 5%;
  display: grid;
  @media (max-width: 1080px) {
    padding: 1rem 5% 1rem 5%;
  }
}
.accentLine{
  height: 3px;
  width: 100%;
}
</style>
