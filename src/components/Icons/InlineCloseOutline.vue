<template>
<svg class="icon inlineCloseOutline" :id="'inlineCloseOutline' + [idCount]" :data-name="'inlineCloseOutline' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineCloseOutline' + [idCount]" viewBox="0 0 32 32">
    <g :id="'inlineCloseOutlineGroup' + [idCount]">
      <circle cx="16" cy="16" r="16" style="fill: none"/>
      <circle cx="16" cy="16" r="15" style="fill: none;stroke-width: 2px"/>
      <line x1="10" y1="22.07" x2="21.87" y2="10" style="fill: none;stroke-miterlimit: 10;stroke-width: 2px"/>
      <line x1="10" y1="10.39" x2="21.73" y2="22.07" style="fill: none;stroke-miterlimit: 10;stroke-width: 2px"/>
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineCloseOutline",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>