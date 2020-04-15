<template>
  <div id="app">
    <horizontal-scroll class="horizontal-scroll">
      <div></div>
    </horizontal-scroll>
  </div>
</template>

<script>
import HorizontalScroll from './components/HorizontalScroll.vue';

export default {
  name: 'App',
  components: {
    HorizontalScroll
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.horizontal-scroll {
  width: 100%;
  height: 100px;
}
</style>
