<template>
<svg class="icon inlineEdit" :id="'inlineEdit' + [idCount]" :data-name="'inlineEdit' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineEdit' + [idCount]" viewBox="0 0 21.74 21.64">
    <g :id="'inlineEditGroup' + [idCount]">
      <path d="M2.17,15,0,21.67,6.72,19.5Z" transform="translate(0 -0.03)" />
      <rect x="3.8" y="7.16" width="14.95" height="6.5" transform="translate(-4.06 10.99) rotate(-45)" />
      <path d="M21.34,3.36l-3-3A1,1,0,0,0,16.93.29a.46.46,0,0,0-.07.07h0l-1,1,4.55,4.55,1-1a1,1,0,0,0,.07-1.41.46.46,0,0,0-.07-.07Z" transform="translate(0 -0.03)" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineEdit",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>