<template>
<svg class="icon suomiTwo" :id="'suomiTwo' + [idCount]" :data-name="'suomiTwo' + [idCount]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 17 27.03">
  <g :id="'ab8bc7ff-6e15-431a-b7d9-5ea37d68dda1' + [idCount]">
    <g :id="'a5f84f2c-9760-4873-9620-0079209680d3' + [idCount]">
      <path d="M16.25,21.72a2.3,2.3,0,0,0-1.14-.31c-.11,0-.21,0-4.84.62-2.21.3-3.86.5-4.94.59l5.94-7.13C15.18,10.87,17,7.73,17,5.61a4.82,4.82,0,0,0-1.07-2.79A6.65,6.65,0,0,0,13.5.69,5.89,5.89,0,0,0,10.9,0,9.09,9.09,0,0,0,8.11.34a7.08,7.08,0,0,0-1.7.78,4.23,4.23,0,0,0-1.15,1,11.84,11.84,0,0,0-.75,1.1l-.19.29-.57.07A2.93,2.93,0,0,0,2.34,4C1.39,4.62,1,5,.91,5.36A2,2,0,0,0,.78,6a2.11,2.11,0,0,0,.69,1.56,2.33,2.33,0,0,0,1.64.61A3.07,3.07,0,0,0,4.93,7.7,6.5,6.5,0,0,0,5.8,7c1.69-1.81,3.27-2.73,4.71-2.73a1.61,1.61,0,0,1,1.11.67,2,2,0,0,1,.63,1.18,7.28,7.28,0,0,1-.08,1.14,3.69,3.69,0,0,1-.48,1,19.09,19.09,0,0,1-1.17,1.66L6.37,15.84a8.24,8.24,0,0,1-.86,1,3.36,3.36,0,0,1-.78.56,5.5,5.5,0,0,0-1.25,1,8.75,8.75,0,0,0-.87,1.06,18.24,18.24,0,0,0-2.1,3.11A4.68,4.68,0,0,0,0,24.47a3,3,0,0,0,.49,1.78A2.52,2.52,0,0,0,2.62,27c1.43,0,3.38-.13,5.78-.37s4.21-.49,5.39-.73h.11a5.07,5.07,0,0,0,.82-.38,2.31,2.31,0,0,0,.85-.63L16,24.6A2.15,2.15,0,0,0,17,23,1.48,1.48,0,0,0,16.25,21.72Z" transform="translate(0 0)"/>
    </g>
  </g>
</svg>
</template>

<script>
export default {
    name: "suomiTwo",
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>