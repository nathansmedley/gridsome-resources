<template>
  <!-- Sets the class of the whole container depending on what mode is selected  -->
  <div
    class="nav"
    v-bind:class="{ dark: mode === 'dark', light: mode === 'light' }"
    @mouseleave="(panel = false), (menu = 'non')"   
  >
    <div class="desktopWrapper" >
      <!-- Top Nav -->
      <div class="topnav" id="topNav">
        <div class="topnav__logo">
          <g-link to="/">
            <img-puller class="topnav__logo__img" ID="moneypenny" />
          </g-link>
        </div>
        <div class="topnav__sections">
          <!-- Hovers set the menu variable and allow the panel to expand -->
          <p
            @mouseover="(panel = true), (menu = 'ser')"
            v-bind:class="{ tabActive: menu === 'ser' }"
          >
            Services
          </p>
          <p
            @mouseover="(panel = true), (menu = 'ind')"
            v-bind:class="{ tabActive: menu === 'ind' }"
          >
            Industries
          </p>
          <p
            @mouseover="(panel = true), (menu = 'res')"
            v-bind:class="{ tabActive: menu === 'res' }"
          >
            Resources
          </p>
          <p
            @mouseover="(panel = true), (menu = 'abo')"
            v-bind:class="{ tabActive: menu === 'abo' }"
          >
            About
          </p>
        </div>
        <div class="topnav__number">
          <div class="topnav__number__phone">
            <Icon bg="none" icon="none"><inline-phone/></Icon>
          </div>
          <g-link class="rulertel" to="tel:03332021005">
            0333 202 1005
          </g-link>
        </div>
        <div class="topnav__refer">
          <g-link to="/referral/">
            Refer and earn £250
          </g-link>
          <div class="topnav__refer__accent">
            <Icon bg="none" icon="none"><accent-thin/></Icon>
          </div>
        </div>
        <div class="topnav__login">
          <g-link to="https://login.moneypenny.com/Account/Login?Region=1">
            Log in 
            <div class="topnav__login__arrow">
              <Icon bg="none" icon="none"><inline-arrow/></Icon>
            </div>
          </g-link>
        </div>
        <div class="topnav__hamburger" @click="mobile = !mobile">
          <transition name="menuFade"
            ><div class="topnav__hamburger__bar" v-show="!mobile"></div
          ></transition>
          <transition name="menuFade"
            ><div class="topnav__hamburger__bar" v-show="!mobile"></div
          ></transition>
          <transition name="menuFade"
            ><div class="topnav__hamburger__bar" v-show="!mobile"></div
          ></transition>
          <transition name="menuFade">
            <div class="topnav__hamburger__cross" v-show="mobile">
              <div class="topnav__hamburger__cross__bar"></div>
              <div class="topnav__hamburger__cross__bar"></div>
            </div>
          </transition>
        </div>
      </div>

      <!-- Nav Drop Down Panels -->

      <transition name="menuFade">
        <!--Shows if panel is true -->
        <div class="navpanel" v-show="panel">
          <!-- Services -->
          <transition name="menuFade">
            <div v-show="menu === 'ser'" class="navpanel__panel serpanel">
              <!-- Calls -->
              <p class="serpanel__title callTitle">Calls</p>
              <g-link
                to="/telephone-answering-service/"
                class="serpanel__pod callPod row1"
              >
                Telephone Answering
                <span>Your own Moneypenny PA</span>
              </g-link>
              <g-link
                to="/outsourced-switchboard/"
                class="serpanel__pod callPod row2"
              >
                Outsourced Switchboard
                <span>Your own 24/7 team of Moneypenny Receptionists</span>
              </g-link>
              <g-link
                to="/small-business-phone-system/"
                class="serpanel__pod callPod row3"
                @click="(panel = false), (menu = 'non')"
              >
                Pocket Phone System
                <span>The power of an office phone system, on your mobile</span>
              </g-link>
              <!-- Chats -->
              <p class="serpanel__title chatTitle">Chats</p>
              <g-link
                to="/outsourced-live-chat/"
                class="serpanel__pod chatPod row1"
              >
                Live Chat
                <span>Chats managed on your behalf</span>
              </g-link>
              <g-link
                to="/self-screening-bot/"
                class="serpanel__pod chatPod row2"
              >
                Self-screening Bot
                <span>An online symptom checker to reassure your customers and staff</span>
              </g-link>
              <!-- More -->
              <p class="serpanel__title moreTitle">More</p>
              <g-link
                to="/business-telephone-numbers/"
                class="serpanel__pod morePod row1"
              >
                Business Telephone Numbers 
                <span>Give your business the phone number it deserves</span>
              </g-link>
              <g-link
                to="/virtual-office-services/"
                class="serpanel__pod morePod row2"
              >
                Virtual Office Services
                <span>Run your business from anywhere with our suite of solutions</span>
              </g-link>
              <g-link
                to="/visitor-management/"
                class="serpanel__pod morePod row3"
              >
                Visitor Management 
                <span>World-leading tech and real people to greet &amp; assist your visitors via video</span>
              </g-link>
            </div>
          </transition>
          <!-- Industries -->
          <transition name="menuFade">
            <div v-show="menu === 'ind'" class="navpanel__panel indpanel">
              <div class="indpanel__pods">
                <g-link
                  to="/legal-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Legal
                  <span>Ranging from sole practitioners to the Magic Circle</span>
                </g-link>
                <g-link
                  to="/accountancy-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Finance
                  <span>Working with hundreds of finance &amp; accountancy professionals</span>
                </g-link>
                <g-link
                  to="/property-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Property
                  <span>#1 provider to the industry for over a decade</span>
                </g-link>
                <g-link
                  to="/franchise-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Franchise
                  <span>Recommended by the British Franchise Association</span>
                </g-link>
                <g-link
                  to="/automotive-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Automotive
                  <span>Supporting local dealers and global brands</span>
                </g-link>
                <g-link
                  to="/small-business-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Small Business
                  <span>Trusted by 21,000 businesses of every kind</span>
                </g-link>
                <g-link
                  to="/healthcare-answering-services/"
                  class="indpanel__pods__pod"
                >
                  Healthcare
                  <span>Preferred supplier to the healthcare industry</span>
                </g-link>
                <g-link to="/enterprise/" class="indpanel__pods__pod">
                  Enterprise
                  <span
                    >Outsourced multichannel communications for larger businesses</span
                  >
                </g-link>
              </div>
              <div class="indpanel__feature">
                <div class="indpanel__feature__text">
                  <p>
                    Our expertise goes far beyond these
                    <span>specialist</span> industries, we serve businesses of
                    every shape and sector.
                  </p>
                </div>
              </div>
            </div>
          </transition>
          <!-- Resources -->
          <transition name="menuFade">
            <div v-show="menu === 'res'" class="navpanel__panel respanel">
              <div class="respanel__pods">
                <g-link
                  to="https://www.moneypenny.com/uk/resources/product-guides/"
                  class="respanel__pods__pod"
                >
                  Product Guides
                  <span
                    >Take a closer look at our products and associated features to understand which one’s right for you</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/articles/case-studies/"
                  class="respanel__pods__pod"
                >
                  Case Studies
                  <span
                    >See what our clients across the many industries we support have to say about our services</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/events/"
                  class="respanel__pods__pod"
                >
                  Events
                  <span
                    >Discover where you can catch us at one of the many events we host, attend or speak at</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/articles/news/"
                  class="respanel__pods__pod"
                >
                  News
                  <span
                    >Read all of our latest press releases, including new appointments, collaborations &amp; growth stories</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/articles/blog/"
                  class="respanel__pods__pod"
                >
                  Blog
                  <span
                    >Check out our new services &amp; best practice write-ups to help make your business even more successful</span
                  >
                </g-link>
              </div>
              <div class="respanel__feature">
                <div class="respanel__feature__img">
                  <img-puller ID="treehouse"/>
                </div>
                <div class="respanel__feature__text">
                  <p>
                    Your one-stop shop for anything and
                    <span>everything</span> Moneypenny.
                  </p>
                </div>
              </div>
            </div>
          </transition>
          <!-- About -->
          <transition name="menuFade">
            <div v-show="menu === 'abo'" class="navpanel__panel abopanel">
              <div class="abopanel__pods">
                <g-link
                  to="/about-us/"
                  class="abopanel__pods__pod"
                >
                  About Us
                  <span
                    >The UK’s leading provider of outsourced telephone &amp; web-based communications to businesses of all shapes and sizes</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/us/"
                  class="abopanel__pods__pod"
                >
                  USA
                  <span
                    >On hand to look after calls & chats for US businesses from our Atlanta, GA office since 2014</span
                  >
                </g-link>
                <g-link
                  to="https://login.moneypenny.com/Account/Login?Region=1"
                  class="abopanel__pods__pod"
                >
                  Client Portal
                  <span
                    >Access to a goldmine of tailored management information to help our clients improve their customer journey</span
                  >
                </g-link>
                <g-link
                  to="/work-with-us/"
                  class="abopanel__pods__pod"
                >
                  Careers
                  <span
                    >View our latest vacancies and come join one of the the fastest growing companies in the UK</span
                  >
                </g-link>
                <g-link
                  to="https://wemindthegap.org.uk/"
                  class="abopanel__pods__pod"
                >
                  WeMindTheGap
                  <span
                    >Our own social mobility charity, set up in 2014 by Moneypenny co-founder, Rachel Clacher</span
                  >
                </g-link>

                <div class="abopanel__logos">
                  <img-puller
                    class="abopanel__logos__img"
                    v-if="mode === 'light'"
                    ID="tp"
                  />
                  <img-puller
                    class="abopanel__logos__img"
                    v-if="mode === 'dark'"
                    ID="tpWhite"
                  />
                  <img-puller class="abopanel__logos__img" ID="bestCompanies" />
                  <img-puller class="abopanel__logos__img" ID="cyber" />
                  <p class="abopanel__logos__text">
                    Collaborating with leading organisations
                  </p>
                  <img-puller
                    class="abopanel__logos__img"
                    v-if="mode === 'light'"
                    ID="microsoft"
                  />
                  <img-puller
                    class="abopanel__logos__img"
                    v-if="mode === 'dark'"
                    ID="microsoftWhite"
                  />
                  <img-puller
                    class="abopanel__logos__img"
                    v-if="mode === 'light'"
                    ID="amazon"
                  />
                  <img-puller
                    class="abopanel__logos__img"
                    v-if="mode === 'dark'"
                    ID="amazonWhite"
                  />
                </div>
              </div>
              <div class="abopanel__feature">
                <div class="abopanel__feature__pod">
                  <p class="abopanel__feature__pod__top">6<span>X</span></p>
                  <p class="abopanel__feature__pod__text">
                    featured for over a decade in The Sunday Times Top 100 Best
                    Companies to Work For
                  </p>
                  <div class="abopanel__feature__pod__line"></div>
                </div>
                <div class="abopanel__feature__pod">
                  <p class="abopanel__feature__pod__top"><span>No.</span>1</p>
                  <p class="abopanel__feature__pod__text">
                    the world’s leading &amp; most trusted outsourced
                    communications partner
                  </p>
                  <div class="abopanel__feature__pod__line"></div>
                </div>
                <div class="abopanel__feature__pod">
                  <p class="abopanel__feature__pod__top"><span>20m</span></p>
                  <p class="abopanel__feature__pod__text">
                    calls &amp; chats looked after on behalf of sole traders to
                    global enterprises
                  </p>
                  <div class="abopanel__feature__pod__line"></div>
                </div>
                <div class="abopanel__feature__pod">
                  <p class="abopanel__feature__pod__top">24<span>/7</span></p>
                  <p class="abopanel__feature__pod__text">
                    every customer managed seamlessly around the clock in our UK
                    head office
                  </p>
                  <div class="abopanel__feature__pod__line"></div>
                </div>
              </div>
            </div>
          </transition>
        </div>
      </transition>
    </div>
    <transition name="menuSlide">
      <div v-show="mobile" class="mobpanel">
        <div
          :class="[{ accActive: mobmenu === 'ser' }, 'accTitle']"
          @click="mobmenu = 'ser'"
          v-scroll-to="'#topNav'"
        >
          Services
        </div>
        <transition name="menuSlide">
          <div class="serpanel" v-show="mobmenu === 'ser'">
            <!-- Calls -->
            <p class="serpanel__title callTitle">Calls</p>
            <g-link
              to="/telephone-answering-service/"
              class="serpanel__pod callPod row1"
            >
              Telephone Answering
              <span>Your own Moneypenny PA</span>
            </g-link>
            <g-link
              to="/outsourced-switchboard/"
              class="serpanel__pod callPod row2"
            >
              Outsourced Switchboard
              <span>Your own 24/7 team of Moneypenny Receptionists</span>
            </g-link>
            <g-link
              to="/small-business-phone-system/"
              class="serpanel__pod callPod row3"
            >
              Pocket Phone System
              <span>The power of an office phone system, on your mobile</span>
            </g-link>
            <!-- Chats -->
            <p class="serpanel__title chatTitle">Chats</p>
            <g-link
              to="/outsourced-live-chat/"
              class="serpanel__pod chatPod row1"
            >
              Live Chat
              <span>Chats managed on your behalf</span>
            </g-link>
            <g-link
              to="/self-screening-bot/"
              class="serpanel__pod chatPod row2"
            >
              Self-screening Bot
              <span>An online symptom checker to reassure your customers and staff</span>
            </g-link>
            <!-- More -->
            <p class="serpanel__title moreTitle">More</p>
            <g-link
              to="/business-telephone-numbers/"
              class="serpanel__pod morePod row1"
            >
              Business Telephone Numbers 
              <span>Give your business the phone number it deserves</span>
            </g-link>
            <g-link
                to="/virtual-office-services/"
                class="serpanel__pod morePod row2"
              >
                Virtual Office Services
                <span>Run your business from anywhere with our suite of solutions</span>
              </g-link>
            <g-link
              to="/visitor-management/"
              class="serpanel__pod morePod row3"
            >
              Visitor Management 
              <span>World-leading tech and real people to greet &amp; assist your visitors via video</span>
            </g-link>
          </div>
        </transition>

        <div
          :class="[{ accActive: mobmenu === 'ind' }, 'accTitle']"
          @click="mobmenu = 'ind'"
          v-scroll-to="'#topNav'"
        >
          Industries
        </div>
        <transition name="menuSlide">
          <div class="indpanel" v-show="mobmenu === 'ind'">
            <div class="indpanel__pods">
              <g-link
                to="/legal-answering-services/"
                class="indpanel__pods__pod"
              >
                Legal
                <span>Ranging from sole practitioners to the Magic Circle</span>
              </g-link>
              <g-link
                to="/accountancy-answering-services/"
                class="indpanel__pods__pod"
              >
                Finance
                <span>Working with hundreds of finance &amp; accountancy professionals</span
                >
              </g-link>
              <g-link
                to="/property-answering-services/"
                class="indpanel__pods__pod"
              >
                Property
                <span>#1 provider to the industry for over a decade</span>
              </g-link>
              <g-link
                to="/franchise-answering-services/"
                class="indpanel__pods__pod"
              >
                Franchise
                <span>Recommended by the British Franchise Association </span>
              </g-link>
              <g-link
                to="/automotive-answering-services/"
                class="indpanel__pods__pod"
              >
                Automotive
                <span
                  >Supporting local dealers and global brands</span
                >
              </g-link>
              <g-link
                to="/small-business-answering-services/"
                class="indpanel__pods__pod"
              >
                Small Business
                <span>Trusted by 21,000 businesses of every kind</span>
              </g-link>
              <g-link
                to="/healthcare-answering-services/"
                class="indpanel__pods__pod"
              >
                Healthcare
                <span>Preferred supplier to the healthcare industry </span>
              </g-link>
              <g-link to="/enterprise/" class="indpanel__pods__pod">
                Enterprise
                <span
                  >Outsourced multichannel communications for larger businesses</span
                >
              </g-link>
            </div>
            <div class="indpanel__feature">
              <div class="indpanel__feature__text">
                <p>
                  Our expertise goes far beyond these
                  <span>specialist</span> industries, we serve businesses of
                  every shape and sector.
                </p>
              </div>
            </div>
          </div>
        </transition>
        <div
          :class="[{ accActive: mobmenu === 'res' }, 'accTitle']"
          @click="mobmenu = 'res'"
          v-scroll-to="'#topNav'"
        >
          Resources
        </div>
        <transition name="menuSlide">
          <div class="respanel" v-show="mobmenu === 'res'">
            <div class="respanel__pods">
              <g-link
                  to="https://www.moneypenny.com/uk/resources/product-guides/"
                  class="respanel__pods__pod"
                >
                  Product Guides
                  <span
                    >Take a closer look at our products and associated features to understand which one’s right for you</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/articles/case-studies/"
                  class="respanel__pods__pod"
                >
                  Case Studies
                  <span
                    >See what our clients across the many industries we support have to say about our services</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/events/"
                  class="respanel__pods__pod"
                >
                  Events
                  <span
                    >Discover where you can catch us at one of the many events we host, attend or speak at</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/articles/news/"
                  class="respanel__pods__pod"
                >
                  News
                  <span
                    >Read all of our latest press releases, including new appointments, collaborations &amp; growth stories</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/uk/resources/articles/blog/"
                  class="respanel__pods__pod"
                >
                  Blog
                  <span
                    >Check out our new services &amp; best practice write-ups to help make your business even more successful</span
                  >
                </g-link>
            </div>
            <div class="respanel__feature">
              <div class="respanel__feature__img">
                <img-puller ID="treehouse"/>
              </div>
              <div class="respanel__feature__text">
                <p>
                  Your one-stop shop for anything and
                  <span>everything</span> Moneypenny.
                </p>
              </div>
            </div>
          </div>
        </transition>

        <div
          :class="[{ accActive: mobmenu === 'abo' }, 'accTitle']"
          @click="mobmenu = 'abo'"
          v-scroll-to="'#topNav'"
        >
          About
        </div>
        <transition name="menuSlide">
          <div class="abopanel" v-show="mobmenu === 'abo'">
            <div class="abopanel__pods">
              <g-link
                  to="/about-us/"
                  class="abopanel__pods__pod"
                >
                  About Us
                  <span
                    >The UK’s leading provider of outsourced telephone &amp; web-based communications to businesses of all shapes and sizes</span
                  >
                </g-link>
                <g-link
                  to="https://www.moneypenny.com/us/"
                  class="abopanel__pods__pod"
                >
                  USA
                  <span
                    >On hand to look after calls & chats for US businesses from our Atlanta, GA office since 2014</span
                  >
                </g-link>
                <g-link
                  to="https://login.moneypenny.com/Account/Login?Region=1"
                  class="abopanel__pods__pod"
                >
                  Client Portal
                  <span
                    >Access to a goldmine of tailored management information to help our clients improve their customer journey</span
                  >
                </g-link>
                <g-link
                  to="/work-with-us/"
                  class="abopanel__pods__pod"
                >
                  Careers
                  <span
                    >View our latest vacancies and come join one of the the fastest growing companies in the UK</span
                  >
                </g-link>
                <g-link
                  to="https://wemindthegap.org.uk/"
                  class="abopanel__pods__pod"
                >
                  WeMindTheGap
                  <span
                    >Our own social mobility charity, set up in 2014 by Moneypenny co-founder, Rachel Clacher</span
                  >
                </g-link>

              <div class="abopanel__logos">
                <img-puller
                  class="abopanel__logos__img"
                  v-if="mode === 'light'"
                  ID="tp"
                />
                <img-puller
                  class="abopanel__logos__img"
                  v-if="mode === 'dark'"
                  ID="tpWhite"
                />
                <img-puller class="abopanel__logos__img" ID="bestCompanies" />
                <img-puller class="abopanel__logos__img" ID="cyber" />
                <p class="abopanel__logos__text">
                  Collaborating with leading organisations
                </p>
                <img-puller
                  class="abopanel__logos__img"
                  v-if="mode === 'light'"
                  ID="microsoft"
                />
                <img-puller
                  class="abopanel__logos__img"
                  v-if="mode === 'dark'"
                  ID="microsoftWhite"
                />
                <img-puller
                  class="abopanel__logos__img"
                  v-if="mode === 'light'"
                  ID="amazon"
                />
                <img-puller
                  class="abopanel__logos__img"
                  v-if="mode === 'dark'"
                  ID="amazonWhite"
                />
              </div>
            </div>
            <div class="abopanel__feature">
              <div class="abopanel__feature__pod">
                <p class="abopanel__feature__pod__top">6<span>X</span></p>
                <p class="abopanel__feature__pod__text">
                  featured for over a decade in The Sunday Times Top 100 Best
                  Companies to Work For
                </p>
                <div class="abopanel__feature__pod__line"></div>
              </div>
              <div class="abopanel__feature__pod">
                <p class="abopanel__feature__pod__top"><span>No.</span>1</p>
                <p class="abopanel__feature__pod__text">
                  the world’s leading &amp; most trusted outsourced
                  communications partner
                </p>
                <div class="abopanel__feature__pod__line"></div>
              </div>
              <div class="abopanel__feature__pod">
                <p class="abopanel__feature__pod__top"><span>20m</span></p>
                <p class="abopanel__feature__pod__text">
                  calls &amp; chats looked after on behalf of sole traders to
                  global enterprises
                </p>
                <div class="abopanel__feature__pod__line"></div>
              </div>
              <div class="abopanel__feature__pod">
                <p class="abopanel__feature__pod__top">24<span>/7</span></p>
                <p class="abopanel__feature__pod__text">
                  every customer managed seamlessly around the clock in our UK
                  head office
                </p>
                <div class="abopanel__feature__pod__line"></div>
              </div>
            </div>
          </div>
        </transition>
        <div class="mobBottomLinks">
          <g-link class="mobBottomLinks__refer" to="/referral/">
            Refer and earn £250
            <div class="mobBottomLinks__refer__accent">
              <Icon bg="none" icon="none"><accent-thin/></Icon>
            </div>
          </g-link>
          <g-link class="mobBottomLinks__login" to="https://login.moneypenny.com/Account/Login?Region=1">
            Log in
            <div class="mobBottomLinks__login__arrow">
              <Icon bg="none" icon="none"><inline-arrow/></Icon>
            </div>
          </g-link>
          <g-link to="/work-with-us/">Careers</g-link>
          <g-link to="/">Home</g-link>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
import ImgPuller from "./ImgPuller.vue";
import Icon from "../components/Icon.vue";
import InlinePhone from "../components/Icons/InlinePhone.vue";
import InlineArrow from '../components/Icons/InlineArrow.vue';
import AccentThin from '../components/Icons/AccentThin.vue';

export default {
  name: "topNav",
  props: {
    mode: String,
    mobmenu: {
      type: String,
      default: "ser",
    },

    mobile: Boolean,
  },
  data() {
    return {
      menu: "",
      panel: false,
    };
  },
  components: {
    ImgPuller,
    Icon,
    InlineArrow,
    AccentThin,
    InlinePhone,
  },
};
</script>

<style lang="scss">
/////Colours/////
.dark {
  background: $darkpurple;
  color: $white;

  a {
    color: $white;
  }

  .navpanel {
    background: $darkpurple;
    border-color: $purple;
  }

  .tabActive {
    border-color: $samiiGreen;
  }

  .topnav {
    border-color: $purple;

    &__refer__accent {
      fill: $samiiGreen;
    }

    &__number__phone { 
        fill: $white;
    }

    &__login__arrow {
      fill: $white;
    }

    &__hamburger {
      &__bar {
        background-color: $white;
      }

      &__cross {
        &__bar {
          background-color: $white;
        }
      }
    }
  }

  .mobpanel {
    background: $darkpurple;
    border-color: $purple;

    .serpanel,
    .indpanel,
    .respanel,
    .abopanel {
      border-color: $purple;
    }

    .accTitle {
      border-color: $purple;
    }
  }

  .mobBottomLinks {
    &__refer__accent {
      fill: $samiiGreen;
    }

    &__login__arrow {
      fill: $white;
    }
  }

  .serpanel {
    &__title {
      @include mobile {
        border-color: $purple !important;
      }
    }
  }
}

.light {
  background: $white;
  color: $darkpurple;

  a {
    color: $darkpurple;
  }

  .navpanel {
    background: $white;
    border-color: $darkwhite;
  }

  .tabActive {
    border-color: $purple;
  }

  .topnav {
    border-color: $darkwhite;

    &__number__phone { 
        fill: $darkpurple;
    }

    &__refer__accent {
      fill: $blue;
    }

    &__login__arrow {
      fill: $darkpurple;
    }

    &__hamburger {
      &__bar {
        background-color: $purple;
      }

      &__cross {
        &__bar {
          background-color: $purple;
        }
      }
    }
  }

  .mobpanel {
    background: $white;
    border-color: $darkwhite;

    .serpanel,
    .indpanel,
    .respanel,
    .abopanel {
      border-color: $darkwhite;
    }

    .accTitle {
      border-color: $darkwhite;
    }
  }

  .mobBottomLinks {
    &__refer__accent {
      fill: $blue;
    }

    &__login__arrow {
      fill: $darkpurple;
    }
  }

  .serpanel {
    &__title {
      @include mobile {
        border-color: $darkwhite !important;
      }
    }
  }
}

/////Structure/////

.nav {
  position: relative;
  z-index: 9999;
}

//top nav

.topnav {
  display: grid;
  grid-template-columns: 405px auto 160px 210px 120px;
  padding-top: 28px;
  height: 100px;
  align-content: center;
  align-self: center;
  @include p-20-topnav;

  @include smdesktop {
     grid-template-columns: 315px auto 150px 200px 110px;
  }
  
  @include lgtablet {
    grid-template-columns: auto 150px 200px 110px 50px 30px;
    padding-top: 0px;
    height: 128px;
  }

  @include tablet {
    grid-template-columns: auto 150px 200px 50px 30px;
    padding-top: 0px;
    height: 128px;
  }

  @include mobile {
    grid-template-columns: auto 150px 40px 0px;
    padding: 26px 15px 26px 15px;
    height: auto;
    border-bottom: 0;
  }

  &__logo {
    &__img {
      width: 250px;
      height: auto;
      padding-top: 5px;
      padding-left: 30px;

      @include smdesktop { 
        width: 180px;
        padding-top: 8px;
      }

      @include lgtablet { 
        width: 180px;
        padding-top: 5px;
        padding-left: 5%;
      }

      @include tablet { 
        width: 180px;
        padding-top: 5px;
        padding-left: 5%;
      }

      @include mobile {
        width: 120px;
        padding-top: 0;
        padding-left: 0;
        transform: translateY(2px);
      }
    }
  }
  &__sections {

    p {
      display: inline-block;
      margin-right: 55px;
      cursor: pointer;
      border-bottom: solid 2px;
      border-color: transparent;
      position: relative;

      @include smdesktop { margin-right: 35px;}
    }

    @include lgtablet {
      display: none;
    }
    @include tablet {
      display: none;
    }
    @include mobile {
      display: none;
    }
  }
  &__number {
    text-align: left;
    position: relative;
    align-self: center;

    &__phone {
      position: absolute;
      height: 21px;
      width: 24px;
      left: -35px;
      top: 0px;
      @include desktop {
        height: 25px;
        width: 29px;
        left: -40px;
      }
      @include mobile {
        height: 16px;
        width: 18px;
        left: 0px;
        top: 2.5px;
      }
    }

    @include mobile {
      text-align: center;
    }

    a {
      text-decoration: none;
    }
    
  }

  &__refer {
    text-align: left;
    position: relative;
    align-self: center;

    a {
      text-decoration: none;
    }
    
    @include mobile {
      display: none;
    }

    &__accent {
      position: absolute;
      width: 70%;
      left: 0;
      bottom: -3px;

      @include desktop {
        width: 82%;
        bottom: -5px;
      }
    }
  }
  &__login {
    text-align: left;
    align-self: center;
    a {
      text-decoration: none;
      display: block;
    }

    @include tablet {
      display: none;
    }
    @include mobile {
      display: none;
    }

    &__arrow {
      position: relative;
      height: 12px;
      display: inline-block;
      margin-left: 15px;
    }
  }

  &__hamburger {
    display: flex;
    align-self: center;
    justify-self: right;
    position: relative;
    height: 30px;
    width: 35px;

    &__bar {
      height: 4px;
      border-radius: 2px;
      margin-bottom: 5px;
      width: 35px;
      display: block;
      position: absolute;
      @include smdesktop {
        display: none;
      }
      @include desktop {
        display: none;
      }

      &:nth-of-type(1) {
        top: 3px;
      }

      &:nth-of-type(2) {
        top: 13px;
      }

      &:nth-of-type(3) {
        top: 24px;
      }
    }

    &__cross {
      border: solid 3px;
      height: 29px;
      width: 35px;
      border-radius: 50%;
      background: transparent;
      transform: translateY(-3px);
      position: relative;

      &__bar {
        height: 2px;
        width: 20px;
        position: absolute;
        top: 50%;
        left: 50%;

        &:nth-of-type(1) {
          transform: translate(-50%, -50%) rotate(45deg);
        }

        &:nth-of-type(2) {
          transform: translate(-50%, -50%) rotate(-45deg);
        }
      }
    }
  }
}

.navpanel {
  position: absolute;
  top: 128px;
  right: 0;
  min-height: 665px;
  width: 100%;
  background-color: inherit;
  box-shadow: 0 25px 25px 0 #00000072;
  border-top: 2px solid;


  &__panel {
    position: absolute;
  }
}

//services panel

.serpanel {
  display: grid;
  grid-template-columns: repeat(3, 280px);
  grid-column-gap: 100px;
  grid-template-rows: auto 1fr 1fr 1fr;
  grid-template-areas:
    "callTitle chatTitle moreTitle"
    "callPod chatPod morePod"
    "callPod chatPod morePod"
    "callPod chatPod morePod";
  padding: 10px 0px;
  margin-left: 405px;
  margin-right: 140px;

  @include smdesktop {
    margin-left: 315px;
    grid-template-columns: repeat(3, 225px);
    grid-column-gap: 60px;
  }

  @include lgtablet {
    grid-template-columns: repeat(3, 1fr);
    grid-column-gap: 60px;
    padding-bottom: 30px;
  }
  @include tablet {
    grid-template-columns: repeat(3, 1fr);
    grid-column-gap: 40px;
    padding-bottom: 30px;
  }
  @include mobile {grid-template-columns: repeat(3, 1fr);}

  .callTitle {
    grid-area: callTitle;
  }
  .chatTitle {
    grid-area: chatTitle;
  }
  .moreTitle {
    grid-area: moreTitle;
  }
  .callPod {
    grid-area: callPod;
  }
  .chatPod {
    grid-area: chatPod;
  }
  .morePod {
    grid-area: morePod;
  }

  .row1 {
    grid-row: 2;
  }
  .row2 {
    grid-row: 3;
  }
  .row3 {
    grid-row: 4;
  }

  &__title {
    @include p-40-nav;
    margin-bottom: 10px;
    margin-top: 56px;
    
    @include smdesktop { margin-top:34px;}
    @include lgtablet { margin-top: 20px;}
    @include tablet { margin-top: 20px;}
  }

  &__pod {
    @include p-23-nav;
    margin: 20px 0px;
    text-decoration: none;

    @include lgtablet { margin: 25px 0px;}
    @include tablet { margin: 30px 0px;}

    span {
      @include o-15-nav;
      display: block;
      margin-top: 12px;
      padding-right:20px;
    }
  }
}

//Ind and Res panel

.indpanel,
.respanel,
.abopanel {
  display: grid;
  grid-template-columns: auto 768px;
  height: 100%;
  width: 100%;

  @include smdesktop {
    grid-template-columns: auto 436px;
  }

  @include lgtablet {
    grid-template-columns: auto 284px;
  }
  @include tablet {
    grid-template-columns: auto 200px;
  }

  &__pods {
    display: grid;
    grid-template-columns: 255px 255px;
    grid-column-gap: 125px;
    padding-left: 405px;
    padding-top: 50px;
    

    @include smdesktop {
      padding-left: 315px;
      grid-template-columns: 210px 210px;
      grid-column-gap: 30px;
    }

    @include lgtablet {
      grid-template-rows: repeat(3, 1fr);
      grid-template-columns: 165px 165px;
      grid-column-gap: 60px;
    }
    @include tablet {
      grid-template-rows: repeat(3, 1fr);
      grid-template-columns: 140px 140px;
      grid-column-gap: 45px;
    }

    @include smdesktop {
      grid-template-columns: 230px 230px;
      grid-column-gap: 38px;
    }

    &__pod {
      @include p-23-nav;
      margin: 0px;
      text-decoration: none;

      @include smdesktop {

      }

      span {
        @include o-15-nav;
        display: block;
        margin-top: 12px;
      }
    }
  }

  &__feature {
    background: $mikeOrange;
    display: flex;
    align-items: center;
    justify-content: center;

    &__text {
      width: 330px;
      text-align: center;

      @include lgtablet {width: 80%;}
      @include tablet {width: 80%;}

      p {
        @include p-40;
        color: $white;

        span {
          @include s-79;
          color: $darkblue;
        }
      }
    }
  }
}

.indpanel {
  &__pods {
    grid-row-gap: 20px;
    grid-template-rows: repeat(4, 120px);
  }
}

.respanel {
  &__pods {
    grid-row-gap: 30px;
    grid-template-rows: repeat(4, 130px);

    @include lgtablet {grid-template-rows: repeat(3, 130px);}
    @include tablet {grid-template-rows: repeat(3, 130px);}
  }

  &__feature {
    background: $blue;
    display: grid;
    width: 100%;
    height: 665px;
    grid-template-rows: 50% 50%;
    align-items: center;
    justify-items: center;

    &__img {
      height: 100%;
      width: 100%;
      overflow: hidden;

      img {
        width: 101%;
        transform: translateX(-2px);

        @include lgtablet {
          width: unset;
        }
        @include tablet {
          width: unset;
        }
      }
    }

    &__text {
      width: 330px;
      text-align: center;
      @include lgtablet {
        width: unset;
      }
      @include tablet {
        width: unset;
      }

      p {
        @include p-40;
        color: $white;
        margin: 0;

        span {
          @include s-79;
          color: $mikeOrange;
        }
      }
    }
  }
}

.abopanel {

  &__pods {
    grid-row-gap: 30px;
    grid-template-rows: repeat(4, 160px);

    @include smdesktop {grid-template-rows: repeat(4, 140px);}
    @include lgtablet {grid-template-rows: repeat(3, 140px);}
    @include tablet {grid-template-rows: repeat(3, 140px);}
  }

  &__logos {
    grid-row: 3;
    grid-column: 2;
    height: auto;
    display: grid;
    max-width: 300px;
    grid-template-rows: 54px 25px 30px;
    grid-template-columns: repeat(3, auto);
    grid-row-gap: 10px;
    @include smdesktop {
      grid-row: 4;
      grid-column: 1/3;
      max-width: 550px;
      grid-template-rows: 25px 35px;
      grid-template-columns: repeat(8, auto);
    }
    &__img {
      display: flex;
      justify-content: center;
      align-items: center;
      @include smdesktop {
        align-items: flex-end;
      }
      &:nth-of-type(1) {
        @include smdesktop {
          grid-row: 1/3;
          grid-column: 1;
        }
      }
      &:nth-of-type(2) {
        @include smdesktop {
          grid-row: 1/3;
          grid-column: 2;
        }
      }
      &:nth-of-type(3) {
        @include smdesktop {
          grid-row: 1/3;
          grid-column: 3;
        }
        @include mobile {
          display: none;
        }
      }
      &:nth-of-type(4) {
        @include smdesktop {
          grid-row: 2;
          grid-column: 5/7;
        }
        @include mobile {
          display: none;
        }
      }
      &:nth-of-type(5) {
        grid-column: 2/4;
        @include smdesktop {
          grid-row: 2;
          grid-column: 7/9;
        }
        @include mobile {
          display: none;
        }

        svg {
          height: 32px !important;
          transform: translateY(7px);
          @include smdesktop {
            transform: translateY(0px);
          }
        }
      }
      .img {
        img,
        svg,
        iframe {
          max-height: 54px;
          max-width: 100%;
          height: 54px;
          @include smdesktop {
            max-height: 45px;
            max-width: 98px;
          }
          @include lgtablet {
            max-height: 36px;
            max-width: 79px;
          }
          @include tablet {
            max-height: 30px;
            max-width: 66px;
          }
          @include mobile {
            max-height: 38px;
            max-width: 81px;
          }
        }
      }
    }
    &__text {
      grid-row: 2;
      grid-column: 1/4;
      margin: 0;
      text-align: center;
      @include p-14;
      @include smdesktop {
        grid-row: 1;
        grid-column: 5/9;
      }
      @include mobile {
        display: none;
      }
    }
  }

  &__feature {
    background: $mikeOrange;
    display: grid;
    grid-template-rows: 50% 50%;
    grid-template-columns: 50% 50%;
    height: 665px;

    @include lgtablet {
      grid-template-rows: repeat(4, 25%);
      grid-template-columns: 100%;
      padding-top: 10px;
    }
    
    @include tablet {
      grid-template-rows: repeat(4, 25%);
      grid-template-columns: 100%;
      padding-top: 10px;
    }

    &__pod {
      text-align: center;
      position: relative;
      align-self: center;

      &__top {
        margin: 0;
        margin-bottom: 8px;
        
        @include desktop {
          @include font-publico(110px, 110px);
        }
        @include smdesktop {
          @include font-publico(98px, 98px);
        }
        @include lgtablet {
          @include font-publico(60px, 40px);
        }
        @include tablet {
          @include font-publico(50px, 30px);
        }
        @include mobile {
          @include font-publico(20px, 20px);
        }
        color: $darkblue;

        span {
          @include desktop {
            @include font-publico(80px, 110px, 500);
          }
          @include smdesktop {
            @include font-publico(73px, 98px, 500);
          }
          @include lgtablet {
            @include font-publico(47px, 40px, 500);
          }
          @include tablet {
            @include font-publico(40px, 30px, 500);
          }
          @include mobile {
            @include font-publico(10px, 20px, 500);
          }
        }
      }

      &__text {
        @include o-15-nav;
        color: $white;
        max-width: 70%;
        margin: 0px auto 30px;

        @include lgtablet {
          margin: 0px auto 10px;
        }
        @include tablet {
          margin: 0px auto 10px;
        }
        @include mobile {
          margin: 0px auto 10px;
        }
      }

      &__line {
        width: 100px;
        height: 2px;
        background-color: $white;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);

        @include lgtablet {
          max-width: 50%;
        }
        @include tablet {
          max-width: 50%;
        }
        @include mobile {
          max-width: 50%;
        }
      }
    }
  }
}

.mobpanel {
  position: absolute;
  width: 100%;
  padding-bottom: 30px;
  box-shadow: 0px 16px 39px #00000072;
  z-index: 9000;
  border-top: solid 2px;

  .accTitle {
    height: 66px;
    border-bottom: solid 2px;
    display: flex;
    align-items: center;
    position: relative;
    @include p-40-nav;
    cursor: pointer;
    @include margin;
    @include mobile {
      margin: 0 10%;
      max-width: 80%;
    }

    &:after {
      content: "";
      display: block;
      position: absolute;
      right: 5px;
      top: 28px;
      height: 10px;
      width: 10px;
      border-bottom: 2px solid;
      border-left: 2px solid;
      transition: transform 0.5s ease;
      transform: rotate(45deg);
    }
  }

  .accActive {
    border-bottom: none;

    &:after {
      transform: rotate(-45deg);
    }
  }

  .serpanel {
    @include mobile {
      grid-template-areas: unset;
      grid-template-rows: repeat(10, auto);
      grid-template-columns: 100%;

      &__pod {
        grid-area: unset;
        grid-column: 1;
      }

      &__title {
        grid-area: unset;
        grid-column: 1;
        border-top: 2px solid;
        padding-top: 20px;

        &:nth-of-type(1) {
          border-top: none;
          padding: 0px;
        }
      }
    }
  }

  .abopanel {
    @include mobile {
      &__logos {
        grid-template-rows: auto;
      }
    }
  }

  .indpanel,
  .respanel,
  .abopanel {
    @include mobile {
      grid-template-columns: 100%;

      &__pods {
        grid-template-columns: 47% 47%;
        grid-template-rows: unset;
        grid-column-gap: 6%;
        margin: 10px 0px;
        
        &__pod {
          background-color: $purple;
          color: $white;
          padding: 15px;
          border-radius: 8px;
          text-align: center;
        }
      }
    }
  }

  .serpanel,
  .indpanel,
  .respanel,
  .abopanel {
    @include margin;
    border-bottom: solid 2px;
    max-width: 60%;

    @include mobile {
      margin: 0 10%;
      max-width: 80%;
    }

    &__pods {
      padding: 20px 0px;
      @include mobile {
        &__pod {
          span {
            display: none;
          }
        }
      }
    }

    &__feature {
      @include mobile {
        display: none;
      }
    }
  }

  .mobBottomLinks {
    margin: 20px 20%;

    &__login {
      display: inline-block !important;
      position: relative;

      &__arrow {
        width: 17px;
        height: 12px;
        position: absolute;
        left: 45px;
        top: 50%;
        transform: translateY(-50%);
      }

      @include tablet {
        text-align: right;
      }
    }

    &__refer {
      position: relative;
      &__accent {
        display: block;
        position: absolute;
        width: 125px;
        height: 2px;
        bottom: -2px;
        left: 0;
      }
    }

    @include mobile {
      margin: 20px 10%;
    }

    @include lgtablet {
      display: none;
    }

    a {
      display: none;
      margin-top: 15px;
      text-decoration: none;
      @include p-14;

      @include mobile {
        display: block;
      }
    }
  }
}

/////Animations/////

.menuSlide-enter-active {
  transition-duration: 0.5s;
  transition-timing-function: ease-in;
}

.menuSlide-leave-active {
  transition-duration: 0.5s;
  transition-timing-function: ease-out;
}

.menuSlide-enter-to,
.menuSlide-leave {
  max-height: 550px;
  overflow: hidden;
}

.menuSlide-enter,
.menuSlide-leave-to {
  overflow: hidden;
  max-height: 0;
}

.menuFade-enter-active {
  transition-delay: 0.3s;
  transition-duration: 0.5s;
  transition-timing-function: ease-in;
}

.menuFade-leave-active {
  transition-duration: 0.5s;
  transition-timing-function: ease-out;
}

.menuFade-enter-to,
.menuFade-leave {
  opacity: 1;
}

.menuFade-enter,
.menuFade-leave-to {
  opacity: 0;
}
</style>
