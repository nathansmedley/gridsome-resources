<template>
<svg class="icon inlineEmail" :id="'inlineEmail' + [idCount]" :data-name="'inlineEmail' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineEmail' + [idCount]" viewBox="0 0 26.15 20.57">
    <g :id="'inlineEmailGroup' + [idCount]">
        <path d="M23.82,20.55A2.25,2.25,0,0,0,25.35,20l-7.41-7.41-.51.36-1.35,1a8.13,8.13,0,0,1-1.38.7,4.24,4.24,0,0,1-1.61.36h0a4.29,4.29,0,0,1-1.61-.36,7.69,7.69,0,0,1-1.37-.7c-.35-.23-.8-.57-1.35-1l-.52-.37L.8,20a2.27,2.27,0,0,0,1.53.57Z" transform="translate(0 0)"/>
        <path d="M1.48,7.9A8.15,8.15,0,0,1,0,6.63V17.9l6.53-6.53C5.23,10.46,3.54,9.3,1.48,7.9Z" transform="translate(0 0)"/>
        <path d="M24.7,7.9q-3,2-5.07,3.48l6.52,6.52V6.63A8,8,0,0,1,24.7,7.9Z" transform="translate(0 0)"/>
        <path d="M23.82,0H2.34A2.12,2.12,0,0,0,.61.76,3,3,0,0,0,0,2.66a3.47,3.47,0,0,0,.8,2A7.18,7.18,0,0,0,2.51,6.34l3,2.08,2.35,1.63,1.48,1,.21.16.4.29.79.55.76.48a4.56,4.56,0,0,0,.84.39,2.24,2.24,0,0,0,.73.13h0a2.24,2.24,0,0,0,.73-.13,4.19,4.19,0,0,0,.83-.39l.76-.48c.21-.14.48-.32.79-.55l.4-.29.22-.16,1.48-1,5.35-3.72a7.08,7.08,0,0,0,1.78-1.8,3.77,3.77,0,0,0,.71-2.2A2.35,2.35,0,0,0,23.82,0Z" transform="translate(0 0)"/>
    </g>
</svg>
</template>

<script>
export default {
    name: 'inlineEmail',
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>