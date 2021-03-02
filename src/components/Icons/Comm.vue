<template>
<svg class="icon comm" :id="'comm' + [idCount]" :data-name="'comm' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'comm' + [idCount]" viewBox="0 0 83.58 85.07">
    <g :id="'commGroup' + [idCount]">
        <path d="M82.73,35.68a43.71,43.71,0,0,0-1.56-6.36c-.26-.81-.55-1.61-.85-2.4C75.48,14.36,64.81,3.78,51.65.8A22.79,22.79,0,0,0,34.08,3.09C19.67,11.77,3.8,23,.56,40.52c-2.84,15.2,5.38,30.21,18.58,38.31a41.84,41.84,0,0,0,29.12,5.59,43.45,43.45,0,0,0,14-5C77.44,71,86.48,52.7,82.73,35.68"/>
    </g>
</svg>
</template>

<script>
export default {
    name: 'comm',
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>