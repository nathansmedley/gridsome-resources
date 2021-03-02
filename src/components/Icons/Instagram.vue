<template>
<svg class="social instagram" :id="'instagram' + [idCount]" :data-name="'instagram' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'instagram' + [idCount]" viewBox="0 0 28.06 28.06">
    <g :id="'instagramGroup' + [idCount]">
        <path  d="M21,.5H8.09A7.59,7.59,0,0,0,.5,8.09V21a7.6,7.6,0,0,0,7.59,7.6H21a7.62,7.62,0,0,0,7.6-7.6V8.09A7.6,7.6,0,0,0,21,.5ZM14.53,22.2a7.67,7.67,0,1,1,7.67-7.67A7.66,7.66,0,0,1,14.53,22.2ZM22.38,8.67A2.27,2.27,0,1,1,24.65,6.4h0A2.28,2.28,0,0,1,22.38,8.67Z" transform="translate(-0.5 -0.5)" />
        <path  d="M14.53,8.5a6,6,0,1,0,6,6h0A6,6,0,0,0,14.53,8.5Z" transform="translate(-0.5 -0.5)" />
        <path  d="M22.38,5.78a.62.62,0,0,0-.62.62.63.63,0,1,0,.62-.62Z" transform="translate(-0.5 -0.5)" />
    </g>
</svg>
</template>

<script>
export default {
    name: 'instagram',
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>