<template>
    <svg class="icon suomiSix" :id="'suomiSix' + [idCount]" :data-name="'suomiSix' + [idCount]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16.5 32.95">
        <g :id="'be292ee9-a45d-408e-a87e-222c3365d909' + [idCount]">
          <g :id="'be341fee-7390-44fd-bdf6-8daabaaed535' + [idCount]">
            <path d="M15.52,15h0a3.42,3.42,0,0,0-2.87-1.58,7.44,7.44,0,0,0-3.33.91,16.85,16.85,0,0,0-2.78,1.86,31.17,31.17,0,0,1,3.21-6.4,17.73,17.73,0,0,1,1.95-2.2A15,15,0,0,0,14,4.75,3.93,3.93,0,0,0,14.6,3,3.3,3.3,0,0,0,14,1.06,2.51,2.51,0,0,0,11.8,0a2.08,2.08,0,0,0-1.69.83c-.26.34-.61.86-1.07,1.61A96.54,96.54,0,0,0,2.39,15.79C.78,19.91,0,23.1,0,25.55a10.54,10.54,0,0,0,.66,3.56,5.55,5.55,0,0,0,2.21,2.94,5.87,5.87,0,0,0,3.18.9,5.55,5.55,0,0,0,3.07-1.18,15,15,0,0,0,3.42-3.64,23.43,23.43,0,0,0,2.87-5.33,13.88,13.88,0,0,0,1.09-4.75A5.23,5.23,0,0,0,15.52,15Zm-8,13a2.68,2.68,0,0,1-1.47.64,2.72,2.72,0,0,1-.62-.17s-.29-.12-.67-.84A5,5,0,0,1,4.3,25.4a6.22,6.22,0,0,1,.22-1.29A13.24,13.24,0,0,1,5,22.6a3.34,3.34,0,0,0,2.72-1.66,9.19,9.19,0,0,1,2.47-2.54,4.59,4.59,0,0,1,2.11-.94h0a1,1,0,0,1,.15.56,10.5,10.5,0,0,1-.85,3.78,22.69,22.69,0,0,1-2,3.89,8.9,8.9,0,0,1-2.08,2.37Z" transform="translate(0 0)"/>
          </g>
        </g>
    </svg>
</template>

<script>
export default {
    name: "suomiSix",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>