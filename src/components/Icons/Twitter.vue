<template>
    <svg class="social twitter" :id="'twitter' + [idCount]" :data-name="'twitter' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'twitter' + [idCount]" viewBox="0 0 32.41 26.33">
    <g :id="'twitterGroup' + [idCount]">
        <path d="M34.54,3.73a14.14,14.14,0,0,1-3.83,1.05A6.63,6.63,0,0,0,33.63,1.1a13.4,13.4,0,0,1-4.21,1.61A6.64,6.64,0,0,0,17.93,7.25a6.48,6.48,0,0,0,.15,1.52A18.81,18.81,0,0,1,4.38,1.82,6.64,6.64,0,0,0,6.43,10.7a6.54,6.54,0,0,1-3-.82V10a6.66,6.66,0,0,0,5.32,6.52A6.46,6.46,0,0,1,7,16.7a5.81,5.81,0,0,1-1.25-.11A6.7,6.7,0,0,0,12,21.22a13.35,13.35,0,0,1-8.23,2.83A13.86,13.86,0,0,1,2.13,24a18.66,18.66,0,0,0,10.19,3C24.55,26.94,31.23,16.81,31.23,8c0-.29,0-.57,0-.85A13.53,13.53,0,0,0,34.54,3.73Z" transform="translate(-2.13 -0.61)" />
    </g>
    </svg>
</template>

<script>
export default {
    name: 'twitter',
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}    
</script>