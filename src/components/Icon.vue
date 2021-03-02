<template>
  <span class="icon-wrapper" :class="{
    'bgBlue':(bg === 'blue'),
    'bgOrange':(bg === 'orange'),
    'bgDarkblue':(bg === 'darkblue'),
    'bgYellow':(bg === 'yellow'),
    'bgDarkWhite':(bg === 'darkwhite'),
    'bgGreen':(bg === 'green'),
    'bgLightblue':(bg === 'lightblue'),
    'bgPurple':(bg === 'purple'),
    'bgLightPurple':(bg === 'lightpurple'),
    'bgDarkWhite':(bg === 'darkwhite'),
    'bgNone':(bg === 'none'),
    'iconWhite':(icon === 'white'),
    'iconDarkWhite':(icon === 'darkwhite'),
    'iconBlue':(icon === 'blue'),
    'iconOrange':(icon === 'orange'),
    'iconDarkblue':(icon === 'darkblue'),
    'iconYellow':(icon === 'yellow'),
    'iconGreen':(icon === 'green'),
    'iconLightblue':(icon === 'lightblue'),
    'iconDarkpurple':(icon === 'darkpurple'),
    'iconDarkwhite':(icon === 'darkwhite'),
    'iconNone':(icon == 'none'),
    }"
    >
    <svg v-if="rotateDeg === null" class="comm" :id="'comm' + [idCount]" :data-name="'comm' + [idCount]" :style="[rotate]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'comm' + [idCount]" viewBox="0 0 83.58 85.07">
      <g :id="'commGroup' + [idCount]">
        <path d="M82.73,35.68a43.71,43.71,0,0,0-1.56-6.36c-.26-.81-.55-1.61-.85-2.4C75.48,14.36,64.81,3.78,51.65.8A22.79,22.79,0,0,0,34.08,3.09C19.67,11.77,3.8,23,.56,40.52c-2.84,15.2,5.38,30.21,18.58,38.31a41.84,41.84,0,0,0,29.12,5.59,43.45,43.45,0,0,0,14-5C77.44,71,86.48,52.7,82.73,35.68"/>
      </g>
    </svg>
    <svg v-if="rotateDeg != null" class="comm" :id="'comm' + [idCount]" :data-name="'comm' + [idCount]" :style="'transform: rotate(' + [rotateDeg] + 'deg)'" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'comm' + [idCount]" viewBox="0 0 83.58 85.07">
      <g :id="'commGroup' + [idCount]">
        <path d="M82.73,35.68a43.71,43.71,0,0,0-1.56-6.36c-.26-.81-.55-1.61-.85-2.4C75.48,14.36,64.81,3.78,51.65.8A22.79,22.79,0,0,0,34.08,3.09C19.67,11.77,3.8,23,.56,40.52c-2.84,15.2,5.38,30.21,18.58,38.31a41.84,41.84,0,0,0,29.12,5.59,43.45,43.45,0,0,0,14-5C77.44,71,86.48,52.7,82.73,35.68"/>
      </g>
    </svg>
      <slot />
  </span>
</template>

<script>
export default {
    name: 'icon',
    props: {
      bg: {
        type: String,
        default: 'none',
      },
      icon: {
        type: String,
        default: 'white',
      },
      rotateDeg: {
        type: String,
        default: null,
      }
    },
    data() {
      return {
        rotate: {
          transform: "rotate(" + Math.floor(Math.random() * 36) * 10 + "deg)",
        },
          idCount: Math.floor(Math.random() * 1000),
      }
    },
}
</script>

<style lang="scss">
.icon-wrapper {
  position: relative;
  height: 100%;
  display: block;
}
.comm {
  position: relative;
}
.social {
    position: absolute;
    left: 50%;
    top: 27px;
    transform: translate(-50%, -50%);
    width: auto;
    z-index: 5;
    &.facebook {
        height: 43px;
        top: 30px;
        @include smdesktop {
           height: 35px;
           top: 27px; 
        }
        @include lgtablet  {
            height: 27px;
            top: 20px;
        }
        @include tablet {
            height: 22px;
            top: 16px;
        }
        @include mobile {
            height: 27px;
            top: 20px;
        }
    }
    &.twitter {
        height: 27px;
        @include smdesktop {
           height: 22px;
           top: 23px; 
        }
        @include lgtablet  {
            height: 17px;
            top: 18px;
        }
        @include tablet {
           height: 14px; 
           top: 15px;
        }
        @include mobile {
            height: 17px;
            top: 18px;
        }
    }
    &.linkedIn {
        height: 27px;
        top: 24px;
        @include smdesktop {
           height: 22px;
           top: 21px; 
        }
        @include lgtablet  {
            height: 18px;
            top: 16px;
        }
        @include tablet {
            height: 14px;
            top: 13px;
        }
        @include mobile {
            height: 18px;
            top: 16px;
        }
    }
    &.instagram {
        height: 28px;
        @include smdesktop {
           height: 23px; 
           top: 23px;
        }
        @include lgtablet  {
            height: 18px;
            top: 18px;
        }
        @include tablet {
            height: 15px;
            top: 15px;
        }
        @include mobile {
            height: 18px;
            top: 18px;
        }
    }
}
.icon {
    position: absolute;
    width: auto;
    height: 60%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    &.play {
      left: 55%;
    }
    &.gift, &.like, &.open {
      top: 45%;
    }
    &.email, &.off, &.live, &.youtube, &.tick {
      height: 45%;
    }
    &.analytics, &.calendar, &.chart, &.cloud, &.message, &.pause, &.search {
      height: 55%;
    }
    &.announce, &.chat, &.clock, &.dollar, &.earth, &.location, &.settings, &.vip {
      height: 65%;
    }
    &.gift, &.like, &.open, &.pound, &.questions, &.twentyFourSeven, &.phone {
      height: 70%;
    }
    &.bulb, &.headset {
      height: 80%;
    }  
}
.accent {
  position: absolute;
  width: 100%;
  height: auto;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.tasArrows {
  width: 475px;
  height: auto;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  @include smdesktop {
    width: 350px;
  }
  @include lgtablet {
    width: 320px;
  }
  @include tablet {
    width: 405px;
  }
  .dot-start, .dot-middle, .dot-end {
    fill: $lukeblue;
  }
  .arrow-top, .arrow-bottom {
    fill: $blue
  }
}
.bgBlue {
  .comm {
    fill: $blue;
  }
}
.bgOrange {
  .comm {
    fill: $mikeOrange;
  }
}
.bgDarkblue {
  .comm {
    fill: $darkblue;
  }
}
.bgYellow {
  .comm {
    fill: $yellow;
  }
}
.bgDarkWhite {
  .comm {
    fill: $darkwhite;
  }
}
.bgGreen {
  .comm {
    fill: $samiiGreen;
  }
}
.bgLightblue {
  .comm {
    fill: $lukeblue;
  }
}
.bgPurple {
  .comm {
    fill: $purple;
  }
}
.bgLightPurple {
  .comm {
    fill: $lightpurple;
  }
}
.bgDarkWhite {
  .comm {
    fill: $darkwhite;
  }
}
.bgNone {
  .comm {
    display: none;
  }
  .icon {
    height: 100%;
    &.play {
      left: 50%;
    }
    &.gift, &.like, &.open {
      top: 50%;
    }
    &.agree, &.announce, &.chat, &.headset, &.location, &.message, &.phone, &.speech, &.twentyFourSeven {
      top: 50%;
    }
    &.tick {
      top: 50%;
      height: 60%;
    }
    &.email, &.off {
      height: 100%;
    }
    &.analytics, &.calendar, &.chart, &.cloud, &.message, &.pause {
      height: 100%;
    }
    &.gift, &.like, &.open, &.pound, &.questions, &.search, &.twentyFourSeven, &.phone {
      height: 100%;
    }
    &.announce, &.chat, &.clock, &.dollar, &.earth, &.location, &.settings, &.vip {
      height: 100%;
    }
    &.bulb, &.headset {
      height: 100%;
    }  
  }
}
.iconWhite {
  .icon, .accent, .social {
    fill: $white;
  }
  .inlineCloseOutline {
    stroke: $white;
  }
}
.iconDarkWhite {
  .icon, .accent, .social {
    fill: $darkwhite;
  }
  .inlineCloseOutline {
    stroke: $darkwhite;
  }
}
.iconBlue {
  .icon, .accent, .social {
    fill: $blue;
  }
  .inlineCloseOutline {
    stroke: $blue;
  }
}
.iconOrange {
  .icon, .accent, .social {
    fill: $mikeOrange;
  }
  .inlineCloseOutline {
    stroke: $mikeOrange;
  }
}
.iconDarkblue {
  .icon, .accent, .social {
    fill: $darkblue;
  }
  .inlineCloseOutline {
    stroke: $darkblue;
  }
}
.iconYellow {
  .icon, .accent, .social {
    fill: $yellow;
  }
  .inlineCloseOutline {
    stroke: $yellow;
  }
}
.iconGreen {
  .icon, .accent, .social {
    fill: $samiiGreen;
  }
  .inlineCloseOutline {
    stroke: $samiiGreen;
  }
}
.iconLightblue {
  .icon, .accent, .social {
    fill: $lukeblue;
  }
  .inlineCloseOutline {
    stroke: $lukeblue;
  }
}
.iconDarkpurple {
  .icon, .accent, .social {
    fill: $darkpurple;
  }
  .inlineCloseOutline {
    stroke: $darkpurple;
  }
}
.iconDarkwhite {
  .icon, .accent, .social {
    fill: $darkwhite;
  }
  .inlineCloseOutline {
    stroke: $darkwhite;
  }
}
.iconNone {
  .icon, .accent, .social {
    fill: inherit;
  }
  .inlineCloseOutline {
    stroke: inherit;
  }
}
</style>

<!--Usage
<icon bg="orange" icon="white"><facebook/></icon> - This will give an orange comm with the facebook icon
<icon bg="green" icon="darkblue"><inline-suitcase/></icon> - This will give a green comm with a dark blue inline suitcase icon
<icon bg="blue" icon="white"><speech/></icon> - This will give a blue comm with a white speech icon
<icon bg="none" icon="yellow"><accent/></icon> - This will give a transparent comm with a yellow accent icon
-->