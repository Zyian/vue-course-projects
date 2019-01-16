<template>
  <div id="app">
    <Wrapper msg="Dimension"/>


    <div id="bg"></div>
  </div>
</template>

<script>
import Wrapper from './components/Wrapper.vue'

export default {
  name: 'app',
  components: {
    Wrapper
  }
}
</script>

<style lang="scss">
#bg {
  background-image: url('./assets/jeremy-bishop-527439-unsplash.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  display: block;
  height: 100vh;
  background-position: center;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1;
  position: fixed;
  filter: blur(4px);
}
</style>
