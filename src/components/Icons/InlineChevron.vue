<template>
<svg class="icon inlineChevron" :id="'inlineChevron' + [idCount]" :data-name="'inlineChevron' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineChevron' + [idCount]" viewBox="0 0 10.73 19.59">
    <g :id="'inlineChevronGroup' + [idCount]">
      <polygon points="1.45 19.59 0 18.22 7.98 9.8 0 1.38 1.45 0 10.73 9.8 1.45 19.59" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineChevron",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>