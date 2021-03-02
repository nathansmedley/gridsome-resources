<template>
<svg class="icon inlineSearch" :id="'inlineSearch' + [idCount]" :data-name="'inlineSearch' + [idCount]"  xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineSearch' + [idCount]" viewBox="0 0 23.35 23.35">
  <g :id="'inlineSearchGroupOne' + [idCount]">
    <g :id="'inlineSearchSubGroupOne' + [idCount]">
      <g :id="'inlineSearchSubSubGroupOne' + [idCount]">
        <g :id="'inlineSearchSubSubGroupOne' + [idCount]">
          <path :id="'inlineSearchPathOne' + [idCount]" d="M22.81,19.9l-4.13-4.13a11.18,11.18,0,0,1-2.91,2.91l4.13,4.13a2.06,2.06,0,0,0,2.91-2.91Z" transform="translate(0 0)"/>
        </g>
      </g>
      <g :id="'inlineSearchGroupTwo' + [idCount]">
        <g :id="'inlineSearchSubGroupTwo' + [idCount]">
          <path :id="'inlineSearchPathTwo' + [idCount]" d="M9.6,4.12a5.49,5.49,0,1,0,5.49,5.49h0A5.48,5.48,0,0,0,9.61,4.12Z" transform="translate(0 0)"/>
        </g>
      </g>
      <g :id="'inlineSearchGroupThree' + [idCount]">
        <g :id="'inlineSearchSubGroupThree' + [idCount]">
          <path :id="'inlineSearchPathThree' + [idCount]" d="M9.6,0a9.6,9.6,0,1,0,9.6,9.6A9.6,9.6,0,0,0,9.6,0Zm0,16.46A6.86,6.86,0,1,1,16.46,9.6h0A6.86,6.86,0,0,1,9.6,16.46Z" transform="translate(0 0)"/>
        </g>
      </g>
    </g>
  </g>
</svg>

</template>

<script>
export default {
    name: "inlineSearch",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>