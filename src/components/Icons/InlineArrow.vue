<template>
<svg class="icon inlineArrow" :id="'inlineArrow' + [idCount]" :data-name="'inlineArrow' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineArrow' + [idCount]" viewBox="0 0 23.44 16.89">
    <g :id="'inlineArrowGroup' + [idCount]">
      <rect y="7.47" width="21.19" height="2" />
      <path d="M14.36,16.23l-.74-.79,7.12-6.61.39-.36-.39-.37L13.62,1.49l.74-.78L22.7,8.47Z" />
      <path d="M14.38,15.52l7.59-7L14.38,1.41l-.05.06,6.75,6.27.79.73-.79.73-6.75,6.27h.05m-.05,1.42-1.41-1.52,7.48-6.9-7.48-7L14.33,0l9.11,8.47Z" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineArrow",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>