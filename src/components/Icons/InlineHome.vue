<template>
<svg class="icon inlineHome" :id="'inlineHome' + [idCount]" :data-name="'inlineHome' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineHome' + [idCount]" viewBox="0 0 22.41 21.29">
    <g :id="'inlineHomeGroup' + [idCount]">
      <path d="M22,9.46,12,.3a1.14,1.14,0,0,0-1.54,0L.38,9.46a1.14,1.14,0,0,0-.09,1.61h0a1.16,1.16,0,0,0,.85.38H2.76v9.17a.65.65,0,0,0,.64.66H8.92a.65.65,0,0,0,.66-.64v0h0V15.06h3.24v5.57a.67.67,0,0,0,.66.66H19a.67.67,0,0,0,.66-.66h0V11.46h1.6a1.14,1.14,0,0,0,1.15-1.15A1.16,1.16,0,0,0,22,9.46Z" transform="translate(0 0)" />
      <path d="M19.43,1.34h-4.5L20.09,6V2A.68.68,0,0,0,19.43,1.34Z" transform="translate(0 0)" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineHome",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>