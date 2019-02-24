<template>
  <div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style lang="scss">
@import "./assets/scss/config.scss";

body {
  position: fixed;
  margin: 0;
  width: 100%;
  height: 100%;
  // overflow: hidden;
  
  &::before {
    content: "";
    display: block;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    z-index: -2;
    background: url("./assets/krsbi.jpg");
    background-size: cover;
    background-position: center center;
  }

  &::after {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    background: rgba($backgroundColor, 0.85);
  }
}
</style>

