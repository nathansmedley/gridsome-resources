<template>
<svg class="icon inlineCalendar" :id="'inlineCalendar' + [idCount]" :data-name="'inlineCalendar' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'inlineCalendar' + [idCount]" viewBox="0 0 24.55 24.56">
    <g :id="'inlineCalendarGroup' + [idCount]">
      <path d="M20.46,3.07a1,1,0,0,0-1-1H16.37V0H14.32V2.05H11.25V0h-2V2.05H6.14V0h-2V2.05H1a1,1,0,0,0-1,1v2H20.46Z" />
      <path d="M16.35,11.56a7,7,0,0,1,4.11,0V6.14H0v13.3a1,1,0,0,0,1,1H11.56a7.14,7.14,0,0,1,4.78-8.9h0Zm-2-3.38h2v2.05H14.32Zm-5.11,0h2v2.05h-2ZM6.14,18.41h-2v-2h2Zm0-4.09h-2v-2h2Zm0-4.09h-2V8.18h2Zm3.07,2h2v2h-2Z" />
      <path d="M18.41,12.28a6.14,6.14,0,1,0,6.14,6.14h0a6.12,6.12,0,0,0-6.11-6.13Zm.73,6.86a1,1,0,0,1-1.05.24l-3.07-1,.65-1.94,2.47.82,2.62-2.63,1.45,1.45Z" />
    </g>
</svg>
</template>

<script>
export default {
    name: "inlineCalendar",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>