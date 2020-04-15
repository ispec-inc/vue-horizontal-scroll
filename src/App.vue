<template>
  <div id="app">
    <horizontal-scroll class="horizontal-scroll">
      <div class="outer">
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
        <div class="inner-content">content</div>
      </div>
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
  display: flex;
  width: 100%;
  height: 150px;
  border: solid 2px #2c3e50;
}

.outer {
  display: flex;
  flex: 1;
  width: auto;
  height: 100%;
  padding: 0 20px;
  flex-flow: row nowrap;
  align-items: center;
}

.horizontal-scroll::after {
  display: block;
  content: '';
  height: 100%;
  width: 10px;
}

.inner-content {
  display: flex;
  flex-shrink: 0;
  align-items: center;
  justify-content: center;
  width: 100px;
  height: calc(100% - 40px);
  border: solid 1px #2c3e50;
  border-radius: 5px;
}

.inner-content:not(:first-of-type) {
  margin-left: 30px;
}
</style>
