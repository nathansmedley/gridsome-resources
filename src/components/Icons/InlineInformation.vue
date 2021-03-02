<template>
<svg class="icon inlineInformation" :id="'inlineInformation' + [idCount]" :data-name="'inlineInformation' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineInformation' + [idCount]" viewBox="0 0 23 23">
  <g :id="'inlineInformationGroup' + [idCount]">
    <g :id="'inlineInformationSubGroup' + [idCount]">
      <g :id="'inlineInformationSubGroupGroup' + [idCount]">
        <path :id="'inlineInformationPath' + [idCount]" d="M11.6,23A11.5,11.5,0,1,1,23.1,11.5,11.5,11.5,0,0,1,11.6,23ZM13,8.19,9.1,8.64V9l.68.42h0c.5.31.62.37.62,1.19v6.33c0,.82-.12.93-.64,1.08l-.63.16v.45H14.3v-.45L13.69,18c-.54-.14-.63-.23-.63-1.08V10.4a14.48,14.48,0,0,1,.06-1.85V8.31L13,8.2Zm-1.3-4.08a1.44,1.44,0,1,0,1.49,1.44,1.44,1.44,0,0,0-1.49-1.44Z" transform="translate(-0.1 0)"/>
      </g>
    </g>
  </g>
</svg>
</template>

<script>
export default {
    name: "inlineInformation",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>