<template>
<svg class="icon inlineClock" :id="'inlineClock' + [idCount]" :data-name="'inlineClock' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineClock' + [idCount]" viewBox="0 0 22 22">
    <g :id="'inlineClockGroup' + [idCount]">
      <path d="M11,0A11,11,0,1,0,22,11,11,11,0,0,0,11,0Zm5.23,16.71a.91.91,0,0,1-1.29,0h0l-4.59-4.59a.9.9,0,0,1-.26-.64v-6a.92.92,0,0,1,1.83-.19.61.61,0,0,1,0,.19V11.1l4.32,4.32a.91.91,0,0,1,0,1.29h0Z"/>
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineClock",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>