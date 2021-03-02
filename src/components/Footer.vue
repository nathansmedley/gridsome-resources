<template>
  <footer
    id="footer"
    class="footer"
    :class="{ footerDark: mode === 'dark', footerLight: mode === 'light' }"
  >
    <div class="wave"></div>
    <div class="footer__wrapper">
      <div class="footer__wrapper__section footer__wrapper__section--solutions">
        <h3 class="footer__wrapper__section__title">Solutions</h3>
        <div class="footer__wrapper__section__list">
          <p class="footer__wrapper__section__list__subtitle">Calls</p>
          <g-link
            to="/telephone-answering-service/"
            class="footer__wrapper__section__list__content"
            >Telephone Answering</g-link
          >
          <g-link
            to="/outsourced-switchboard/"
            class="footer__wrapper__section__list__content"
            >Outsourced Switchboard</g-link
          >
          <g-link
            to="/small-business-phone-system/"
            class="footer__wrapper__section__list__content"
            >Pocket Phone System</g-link
          >
        </div>
        <div class="footer__wrapper__section__list">
          <p class="footer__wrapper__section__list__subtitle">Chats</p>
          <g-link
            to="/outsourced-live-chat/"
            class="footer__wrapper__section__list__content"
            >Live Chat</g-link
          >
          <g-link
            to="/self-screening-bot/"
            class="footer__wrapper__section__list__content"
            >Self-screening Bot</g-link
          >
        </div>
        <div class="footer__wrapper__section__list">
          <p class="footer__wrapper__section__list__subtitle">More</p>
          <g-link
            to="/business-telephone-numbers/"
            class="footer__wrapper__section__list__content"
            >Business Telephone Numbers</g-link
          >
          <g-link
            to="/visitor-management/"
            class="footer__wrapper__section__list__content"
            >Visitor Management</g-link
          >
          <g-link
            to="/microsoft-teams/"
            class="footer__wrapper__section__list__content"
            >Microsoft Teams</g-link
          >
          <g-link
            to="/virtual-receptionist-service/"
            class="footer__wrapper__section__list__content"
            >Virtual Receptionist</g-link
          >
          <g-link
            to="/virtual-office-services/"
            class="footer__wrapper__section__list__content"
            >Virtual Office Services </g-link
          >
        </div>
      </div>
      <div class="footer__wrapper__section footer__wrapper__section--company">
        <h3 class="footer__wrapper__section__title">Company</h3>
        <div class="footer__wrapper__section__list">
          <g-link
            to="/referral/"
            class="footer__wrapper__section__list__content"
            >Refer &amp; Earn</g-link
          >
          <g-link
            to="https://www.moneypenny.com/uk/resources/"
            class="footer__wrapper__section__list__content"
            >Resources</g-link
          >
          <g-link
            to="/about-us/"
            class="footer__wrapper__section__list__content"
            >About Us</g-link
          >
          <g-link
            to="/work-with-us/"
            class="footer__wrapper__section__list__content"
            >Careers</g-link
          >
          <a
            href="https://login.moneypenny.com/Account/Login?Region=1"
            class="footer__wrapper__section__list__content"
            >Client Portal</a
          >
          <g-link
            to="https://wemindthegap.org.uk/"
            target="_blank"
            class="footer__wrapper__section__list__content"
            >Our Charity</g-link
          >
          <g-link to="https://www.moneypenny.com/us/" class="footer__wrapper__section__list__content">USA</g-link>
        </div>
      </div>
      <div class="footer__wrapper__section footer__wrapper__section--git">
        <h3 class="footer__wrapper__section__title">Get in touch</h3>
        <icon class="footer__wrapper__section__icon" bg="none" icon="white"
          ><inlinePhone
        /></icon>
        <g-link to="tel:03332021005" class="footer__wrapper__section__text rulertel"
          >0333 202 1005</g-link
        >
        <icon class="footer__wrapper__section__icon" bg="none" icon="white"
          ><inlineEmail
        /></icon>
        <g-link
          to="mailto:hello@moneypenny.co.uk"
          class="footer__wrapper__section__text"
          >hello@moneypenny.co.uk</g-link
        >
        <div class="footer__wrapper__section__social">
          <g-link to="https://www.facebook.com/HelloMoneypennyUK">
            <icon
              v-if="mode === 'dark'"
              bg="orange"
              icon="darkpurple"
              ><facebook
            /></icon>
            <icon v-if="mode === 'light'" bg="orange" icon="white"
              ><facebook
            /></icon>
          </g-link>
        </div>
        <div class="footer__wrapper__section__social">
          <g-link to="https://twitter.com/Moneypenny">
            <icon
              v-if="mode === 'dark'"
              bg="orange"
              icon="darkpurple"
              ><twitter
            /></icon>
            <icon v-if="mode === 'light'" bg="orange" icon="white"
              ><twitter
            /></icon>
          </g-link>
        </div>
        <div class="footer__wrapper__section__social">
          <g-link to="https://www.linkedin.com/company/83349">
            <icon
              v-if="mode === 'dark'"
              bg="orange"
              icon="darkpurple"
              ><linked-in
            /></icon>
            <icon v-if="mode === 'light'" bg="orange" icon="white"
              ><linked-in
            /></icon>
          </g-link>
        </div>
        <div class="footer__wrapper__section__social">
          <g-link
            to="https://www.instagram.com/lifeatmoneypenny/?hl=en"
          >
            <icon v-if="mode === 'dark'" bg="orange" icon="darkpurple"
              ><instagram
            /></icon>
            <icon v-if="mode === 'light'" bg="orange" icon="white"
              ><instagram
            /></icon>
          </g-link>
        </div>
      </div>
      <div class="footer__wrapper__section footer__wrapper__section--logos">
        <img-puller class="footer__wrapper__section__logo" ID="bestCompanies" />
        <img-puller class="footer__wrapper__section__logo" ID="cyber" />
        <img-puller
          class="footer__wrapper__section__logo"
          v-if="mode === 'dark'"
          ID="btbWhite"
        />
        <img-puller
          class="footer__wrapper__section__logo"
          v-if="mode === 'light'"
          ID="btb"
        />
        <img-puller
          class="footer__wrapper__section__logo"
          v-if="mode === 'dark'"
          ID="nphWhite"
        />
        <img-puller
          class="footer__wrapper__section__logo"
          v-if="mode === 'light'"
          ID="nph"
        />
      </div>
      <div class="footer__wrapper__section footer__wrapper__section--legal">
        <g-link
          to="/terms-and-conditions/"
          class="footer__wrapper__section__legal"
          >Terms of Use</g-link
        >
        <g-link to="/trademark/" class="footer__wrapper__section__legal"
          >Trademark</g-link
        >
        <g-link to="/modern-slavery/" class="footer__wrapper__section__legal"
          >Modern Slavery</g-link
        >
        <g-link to="/gender-pay-gap/" class="footer__wrapper__section__legal"
          >Gender Pay Gap</g-link
        >
        <g-link to="/privacy/" class="footer__wrapper__section__legal"
          >Privacy Policy</g-link
        >
        <g-link to="/cookies-policy/" class="footer__wrapper__section__legal"
          >Cookies Policy</g-link
        >
        <p
          class="footer__wrapper__section__legal footer__wrapper__section__legal--p"
        >
          &copy; Moneypenny {{ new Date().getFullYear() }}
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import icon from "./Icon.vue";
import inlineEmail from "./Icons/InlineEmail.vue";
import inlinePhone from "./Icons/InlinePhone.vue";
import comm from "./Icons/Comm.vue";
import facebook from "./Icons/Facebook.vue";
import twitter from "./Icons/Twitter.vue";
import linkedIn from "./Icons/LinkedIn.vue";
import instagram from "./Icons/Instagram.vue";
import ImgPuller from "./ImgPuller.vue";

export default {
  name: "bottomFooter",
  props: {
    mode: String,
  },
  components: {
    icon,
    inlineEmail,
    inlinePhone,
    facebook,
    twitter,
    linkedIn,
    instagram,
    ImgPuller,
  },
};
</script>

<style lang="scss">
.footerDark {
  background: $darkpurple;
  color: $white;

  a {
    color: $white;
  }

  .inlinePhone,
  .inlineEmail {
    fill: $white;
  }
}

.footerLight {
  background: $white;
  color: $darkpurple;

  a {
    color: $darkpurple;
  }

  .inlinePhone,
  .inlineEmail {
    fill: $darkpurple;
  }
}

.footer {
  position: relative;
  bottom: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  .wave {
    height: 600px;
    width: 100%;
    position: absolute;
    right: -55%;
    bottom: -15%;
    background-image: url("https://res.cloudinary.com/moneypenny/image/upload/f_auto/v1/UK/Template/commscape-twirl.png");
    background-repeat: no-repeat;
    background-size: 80%;
    background-position: center center;
    @include smdesktop {
      bottom: -20%;
    }
    @include lgtablet {
      right: -45%;
      bottom: -20%;
      transform: rotate(-20deg);
    }
    @include tablet {
      bottom: -25%;
      transform: rotate(-15deg);
    }
    @include mobile {
      width: 200%;
      background-size: 100%;
      right: -70%;
      transform: rotate(20deg);
    }
  }
  &__wrapper {
    display: grid;
    @include margin;
    grid-template-columns: 3fr 1fr 1.5fr;
    grid-template-rows: 1fr 60px 50px;
    grid-column-gap: 50px;
    grid-row-gap: 30px;
    @include paddingTop;
    @include paddingBottom;
    box-sizing: border-box;
    position: relative;
    z-index: 5;
    @include smdesktop {
      grid-template-columns: 3fr 1fr;
      grid-template-rows: 1fr 113px 50px 25px;
    }
    @include lgtablet {
      grid-template-columns: 3fr 1fr;
      grid-template-rows: 1fr 103px 45px 25px;
    }
    @include tablet {
      grid-template-columns: 385px 130px;
      grid-template-rows: 1fr 87px 37px 25px;
      grid-column-gap: 25px;
    }
    @include mobile {
      padding: 60px 15px 200px !important;
      grid-template-columns: 1fr;
      grid-template-rows: 700px 350px 1fr 53px 90px;
      grid-column-gap: 0;
      grid-row-gap: 40px;
      width: 100% !important;
      max-width: initial !important;
    }
    &__section {
      display: grid;
      grid-template-rows: 1fr 4fr;
      letter-spacing: 0;
      text-align: left;
      grid-column-gap: 10px;
      &--solutions {
        grid-template-columns: 1.5fr 1fr 1.2fr;
        .footer__wrapper__section__title {
          grid-column: 1/4;
        }
        @include smdesktop {
          grid-template-columns: repeat(3, 1fr);
        }
        @include lgtablet {
          grid-template-columns: repeat(3, 1fr);
        }
        @include tablet {
          grid-template-columns: 1.3fr 1fr 1.2fr;
        }
        @include mobile {
          grid-template-columns: 1fr;
          grid-template-rows: 70px 225px 125px 245px;
          grid-row-gap: 15px;
          grid-column-gap: 0;
        }
      }
      &--company {
        grid-template-columns: 1fr;
        @include mobile {
          grid-row: 2;
          grid-column: 1;
        }
      }
      &--git {
        grid-template-rows: 83px 45px 45px 1fr;
        grid-template-columns: 30px 10px 50px 50px 50px;
        .footer__wrapper__section__title {
          grid-column: 1/6;
        }
        @include smdesktop {
          grid-row: 2;
          grid-template-rows: 70px 43px;
          grid-template-columns: 30px 150px 30px 250px 43px 43px 43px 43px;
        }
        @include lgtablet {
          grid-row: 2;
          grid-template-rows: 70px 33px;
          grid-template-columns: 23px 120px 23px 200px 33px 33px 33px 33px;
        }
        @include tablet {
          grid-row: 2;
          grid-template-rows: 60px 27px;
          grid-template-columns: 23px 100px 23px 170px 27px 27px 27px 27px;
        }
        @include mobile {
          grid-row: 3;
          grid-template-rows: 70px 20px 20px 33px;
          grid-template-columns: repeat(5, 34px);
          grid-row-gap: 15px;
        }
      }
      &--logos {
        grid-template-columns: 59px 71px 121px 160px;
        grid-template-rows: 60px;
        grid-row: 2;
        grid-column: 1/3;
        grid-column-gap: 30px;
        @include smdesktop {
          grid-row: 3;
          grid-template-columns: 51px 61px 105px 138px;
          grid-template-rows: 50px;
        }
        @include lgtablet {
          grid-row: 3;
          grid-template-columns: 44px 53px 90px 120px;
          grid-column-gap: 18px;
          grid-template-rows: 45px;
        }
        @include tablet {
          grid-row: 3;
          grid-template-columns: 37px 45px 76px 100px;
          grid-column-gap: 15px;
          grid-template-rows: 37px;
        }
        @include mobile {
          grid-row: 4;
          grid-template-columns: 43px 52px 88px 115px;
          grid-column-gap: 15px;
          grid-template-rows: 43px;
        }
      }
      &--legal {
        grid-row: 3;
        grid-column: 1/3;
        grid-template-columns: repeat(7, max-content);
        grid-template-rows: 50px;
        grid-column-gap: 30px;
        @include smdesktop {
          grid-row: 4;
          grid-template-rows: 25px;
        }
        @include lgtablet {
          grid-row: 4;
          grid-template-rows: 25px;
        }
        @include tablet {
          grid-column-gap: 17px;
          grid-row: 4;
          grid-template-rows: 25px;
        }
        @include mobile {
          grid-row: 5;
          grid-template-columns: repeat(3, auto);
          grid-column-gap: 15px;
          grid-template-rows: repeat(3, 20px);
          grid-row-gap: 15px;
        }
      }
      &__title {
        @include p-40;
        margin: 15px 0;
        margin-top:0;
      }
      &__list {
        grid-row-start: 2;

        @include desktop {
          padding-right:15px;
        }
        @include mobile {
          grid-row-start: auto;
          grid-column: 1;
        }
        &__subtitle {
          @include p-23-footer;
          margin: 10px 0;
        }
        &__content {
          @include o-16-footer;
          margin: 15px 0;
          text-decoration: none;
          display: block;
        }
      }
      &__icon {
        width: 30px;
        height: 25px;
        grid-column: 1;
        position: relative;
        top: 50%;
        transform: translateY(-50%);
        &:nth-child(4) {
          @include smdesktop {
            grid-column: 3;
            grid-row: 2;
          }
          @include lgtablet {
            grid-column: 3;
          }
          @include tablet {
            grid-column: 3;
          }
        }
        @include lgtablet {
          width: 23px;
          height: 22px;
          grid-column: 1;
          grid-row: 2;
        }
        @include tablet {
          width: 19px;
          height: 18px;
          grid-column: 1;
          grid-row: 2;
        }
        @include mobile {
          width: 23px;
          height: 22px;
        }
      }
      &__text {
        @include p-20-footer;
        grid-column: 2/6;
        margin: 0;
        text-decoration: none;
        display: flex;
        align-self: center;
        &:first-of-type {
          @include smdesktop {
            grid-column: 2;
          }
          @include lgtablet {
            grid-column: 2;
          }
          @include tablet {
            grid-column: 2;
          }
        }
        @include smdesktop {
          grid-column: 4;
          grid-row: 2;
        }
        @include lgtablet {
          grid-column: 4;
          grid-row: 2;
        }
        @include tablet {
          grid-column: 4;
          grid-row: 2;
        }
      }
      &__social {
        margin: 35px 0;
        grid-row: 4;
        position: relative;
        @include smdesktop {
          grid-row: 2;
          margin: 0;
        }
        @include lgtablet {
          grid-row: 2;
          margin: 0;
        }
        @include tablet {
          grid-row: 2;
          margin: 0;
        }
        @include mobile {
          grid-row: 4;
          margin: 0;
        }
        &:nth-child(6) {
          grid-column: 1/3;
          @include smdesktop {
            grid-column: 5;
          }
          @include lgtablet {
            grid-column: 5;
          }
          @include tablet {
            grid-column: 5;
          }
          @include mobile {
            grid-column: 1;
          }
        }
        &:nth-child(7) {
          grid-column: 3;
          @include smdesktop {
            grid-column: 6;
          }
          @include lgtablet {
            grid-column: 6;
          }
          @include tablet {
            grid-column: 6;
          }
          @include mobile {
            grid-column: 2;
          }
        }
        &:nth-child(8) {
          grid-column: 4;
          @include smdesktop {
            grid-column: 7;
          }
          @include lgtablet {
            grid-column: 7;
          }
          @include tablet {
            grid-column: 7;
          }
          @include mobile {
            grid-column: 3;
          }
        }
        &:nth-child(9) {
          grid-column: 5;
          @include smdesktop {
            grid-column: 8;
          }
          @include lgtablet {
            grid-column: 8;
          }
          @include tablet {
            grid-column: 8;
          }
          @include mobile {
            grid-column: 4;
          }
        }
      }
      &__logo {
        height: auto;
        width: 100%;
        display: flex;
        align-self: flex-end;
        .img {
          height: auto;
          width: 100%;
          img,
          svg {
            height: auto;
            width: 100%;
          }
        }
      }
      &__legal {
        @include o-13-footer;
        text-decoration: none;
        margin: 0;
        &--p {
          @include mobile {
            grid-row: 3;
            grid-column: 1/4;
          }
        }
      }
    }
  }
}
</style>
