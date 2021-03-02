<template>
    <svg class="social facebook" :id="'facebook' + [idCount]" :data-name="'facebook' + [idCount]" xmlns="http://www.w3.org/2000/svg" :aria-labelledby="'facebook' + [idCount]" viewBox="0 0 21.32 42.63">
        <g :id="'facebookGroup' + [idCount]">
            <path d="M17.93,7.58h3.89V.8A48.84,48.84,0,0,0,16.15.5C10.54.5,6.69,4,6.69,10.52v6H.5v7.57H6.69V43.13h7.6V24.07h5.94l.94-7.58H14.28V11.27C14.28,9.08,14.88,7.58,17.93,7.58Z" transform="translate(-0.5 -0.5)" />
        </g>
    </svg>
</template>

<script>
export default {
    name: 'facebook',
    data() {
      return {
        idCount: Math.floor(Math.random() * 1000),
      }
    }
}
</script>