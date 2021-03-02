<template>
<svg class="icon inlineCloseSolid" :id="'inlineCloseSolid' + [idCount]" :data-name="'inlineCloseSolid' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineCloseSolid' + [idCount]" viewBox="0 0 31 31">
    <g :id="'inlineCloseSolidGroup' + [idCount]">
      <path d="M15.51,31a15.5,15.5,0,1,1,11-4.54A15.5,15.5,0,0,1,15.51,31ZM12,11a1,1,0,0,0-1,1,1,1,0,0,0,.3.7l2.83,2.83L11.3,18.36a1,1,0,0,0,0,1.41h0a1,1,0,0,0,1.41,0h0L15.54,17l2.83,2.82A1,1,0,1,0,20,18.6l-.1-.12-.11-.12L17,15.53l2.82-2.83a1,1,0,0,0,0-1.41A1,1,0,0,0,19,11a1,1,0,0,0-.7.29l-2.83,2.83-2.83-2.83A1,1,0,0,0,12,11Z" transform="translate(-0.05 0)" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineCloseSolid",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>