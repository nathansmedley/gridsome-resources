<template>
<svg class="icon inlineBack" :id="'inlineBack' + [idCount]" :data-name="'inlineBack' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineBack' + [idCount]" viewBox="0 0 21.49 21.47">
    <g :id="'inlineBackGroup' + [idCount]">
      <path d="M8.44,4.62V.77A.76.76,0,0,0,7.67,0,.73.73,0,0,0,7.1.26L.2,7.92a.76.76,0,0,0,0,1l6.9,8.43a.76.76,0,0,0,1.08.11.74.74,0,0,0,.28-.59V13.05c6.06.2,9.84,2.79,11.54,7.9a.78.78,0,0,0,.73.52h.12a.78.78,0,0,0,.65-.75C21.47,11.67,16,5,8.44,4.62Z" transform="translate(-0.01 0)" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineBack",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>