<template>
  <div class="layout">
    <slot/>
  </div>
</template>

<style>
body {
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.rulertel {
  color: inherit;
  text-decoration: none;
}
img {
  max-width: 100%;
}
.header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.nav__link {
  margin-left: 20px;
}
.post-list {
  list-style: none;
  padding-left: 0;
}
.post-list li {
  padding: 1em 0;
}
</style>
