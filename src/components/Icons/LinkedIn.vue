<template>
<svg class="social linkedIn" :id="'linkedIn' + [idCount]" :data-name="'linkedIn' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'linkedIn' + [idCount]" viewBox="0 0 29.34 26.79">
    <g :id="'linkedInGroup' + [idCount]">
        <path d="M1.45,27.29H5.26a1,1,0,0,0,1-.95V9.67a1,1,0,0,0-1-.95H1.45a1,1,0,0,0-.95.95V26.33a1,1,0,0,0,1,1Z" transform="translate(-0.5 -0.5)" />
        <path d="M1.45,5.79H5.26a1,1,0,0,0,1-1V1.45a1,1,0,0,0-1-.95H1.45a1,1,0,0,0-.95,1V4.84A1,1,0,0,0,1.45,5.79Z" transform="translate(-0.5 -0.5)" />
        <path d="M28.39,10.65A5.79,5.79,0,0,0,26,8.91a8.72,8.72,0,0,0-3.46-.68,8.48,8.48,0,0,0-6.51,2.93c-.35.39-.61.3-.61-.22V9.67a1,1,0,0,0-.95-.95h-3.4a1,1,0,0,0-.95.95V26.34a1,1,0,0,0,.95.95H14.9a1,1,0,0,0,.95-.95v-5.8a18.86,18.86,0,0,1,.44-5,4.11,4.11,0,0,1,1.62-2.16,4.58,4.58,0,0,1,2.66-.81,3.42,3.42,0,0,1,2,.57,3.18,3.18,0,0,1,1.19,1.6,17.24,17.24,0,0,1,.36,4.53v7a1,1,0,0,0,1,1h3.81a1,1,0,0,0,.95-1V16.9a17.77,17.77,0,0,0-.31-3.85A6.31,6.31,0,0,0,28.39,10.65Z" transform="translate(-0.5 -0.5)" />
    </g>
</svg> 
</template>

<script>
export default {
    name: 'linkedIn',
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>