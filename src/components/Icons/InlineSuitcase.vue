<template>
<svg class="icon inlineSuitcase" :id="'inlineSuitcase' + [idCount]" :data-name="'inlineSuitcase' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineSuitcase' + [idCount]" viewBox="0 0 27.15 22.63">
    <g :id="'inlineSuitcaseGroup' + [idCount]">
      <path d="M17,5.09A1.14,1.14,0,0,1,15.84,4V2.26H11.31V4A1.13,1.13,0,0,1,9.05,4V2.26A2.26,2.26,0,0,1,11.31,0h4.53A2.26,2.26,0,0,1,18.1,2.26h0V4A1.13,1.13,0,0,1,17,5.09Z" transform="translate(0 0)" />
      <path d="M14.38,15.14a2.2,2.2,0,0,1-.8.13,2.57,2.57,0,0,1-.87-.15L0,10.88v8.64a3.11,3.11,0,0,0,3.11,3.11H24a3.11,3.11,0,0,0,3.11-3.11h0V10.88Z" transform="translate(0 0)" />
      <path d="M27.15,6.51V9.09l-13.3,4.44a.83.83,0,0,1-.54,0L0,9.09V6.51A3.12,3.12,0,0,1,3.11,3.39H24a3.11,3.11,0,0,1,3.15,3.07v0Z" transform="translate(0 0)" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineSuitcase",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>