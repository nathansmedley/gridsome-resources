<template>
<svg class="icon suomiOne" :id="'suomiOne' + [idCount]" :data-name="'suomiOne' + [idCount]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 7.05 26.95">
  <g :id="'ab54d514-43ff-4b10-bee8-e3f0129e50bc' + [idCount]">
    <g :id="'a9f0190b-347a-4fbf-835a-439daf90a5f2' + [idCount]">
      <path d="M7.05,3.17a2.34,2.34,0,0,0-.56-1.43h0A2,2,0,0,0,5.79.53,2,2,0,0,0,4.44,0c-.52,0-1,.26-1.9,1.09A9,9,0,0,0,1,2.87,4.17,4.17,0,0,0,.29,4.63,2,2,0,0,0,.63,6a1.91,1.91,0,0,0,1.52.92h0c0,.84-.26,3.08-1.08,8.75C0,23.37,0,23.59,0,23.75a3.49,3.49,0,0,0,.63,2A2.45,2.45,0,0,0,2.7,27h0c.47,0,2-.19,2-2.62L4.37,22.7h0A84.93,84.93,0,0,1,5.54,14c1-6.29,1.2-7.82,1.21-8.35l.3-2.42Z"/>
    </g>
  </g>
</svg>
</template>

<script>
export default {
    name: "suomiOne",
    data() {
        return {
            idCount: Math.floor(Math.random() * 1000),
        }
    }
}
</script>