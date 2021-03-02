<template>
    <svg class="icon inlineTick" :id="'inlineTick' + [idCount]" :data-name="'inlineTick' + [idCount]"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18.5 18.5">
      <g>
        <circle cx="9.25" cy="9.25" r="9.25"/>
        <path d="M14.12,4.35,7.58,10.89,4.38,7.68,2.75,9.31l4.83,4.83L15.75,6Z" style="fill: #fff"/>
      </g>
    </svg>
</template>

<script>
export default {
    name: "inlineTick",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>