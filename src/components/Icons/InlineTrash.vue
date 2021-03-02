<template>
<svg class="icon inlineTrash" :id="'inlineTrash' + [idCount]" :data-name="'inline-Trash' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineTrash' + [idCount]" viewBox="0 0 19.81 25.17">
  <g :id="'inlineTrashGroupOne' + [idCount]">
    <g :id="'inlineTrashSubGroupOne' + [idCount]">
      <g :id="'inlineTrashSubSubGroupOne' + [idCount]">
        <path :id="'inlineTrashPathOne' + [idCount]" d="M19.05,7.13a.74.74,0,0,0,.74-.74.63.63,0,0,0-.06-.27A4.68,4.68,0,0,0,15.4,3.2h-.9A3.93,3.93,0,0,0,10.68,0H9.1A3.92,3.92,0,0,0,5.29,3.2H4.38A4.7,4.7,0,0,0,.05,6.12a.74.74,0,0,0,.37,1l0,0a.62.62,0,0,0,.27,0ZM9.1,1.48h1.58A2.42,2.42,0,0,1,13,3.2H6.81A2.42,2.42,0,0,1,9.1,1.48Z" transform="translate(0.02 0)"/>
        <path :id="'inlineTrashPathTwo' + [idCount]" d="M2.77,23.12A2.21,2.21,0,0,0,5,25.17h9.84A2.21,2.21,0,0,0,17,23.12L18,8.6H1.73Zm9.14-10.57a.74.74,0,0,1,1.48.07L13,20.49a.73.73,0,0,1-.78.67h0a.75.75,0,0,1-.67-.74Zm-4.8-.7a.74.74,0,0,1,.77.7l.39,7.87a.74.74,0,0,1-.78.7.76.76,0,0,1-.69-.63l-.4-7.87a.74.74,0,0,1,.7-.77Z" transform="translate(0.02 0)"/>
      </g>
    </g>
  </g>
</svg>
</template>

<script>
export default {
    name: "inlineTrash",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>