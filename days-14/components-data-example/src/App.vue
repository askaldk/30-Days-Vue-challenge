<template>
  <div id="app">
    <p>Three different components.</p>
    <counter></counter>
  </div>
</template>

<script>
import counter from './components/couter1.vue'
export default {
  name: 'app',
  components:{
    counter
  }
}
</script>

<style>
html, body {
  height: 100%;
  padding-top: 10px;
  background: #e6ecf1;
}

#app {
  height: 100%;
  max-width: 1000px;
  padding: 12px;
}

p {
  padding-bottom: 5px;
}

.component-button {
  margin-left: 10px;
  display: inline-block;
  margin-top: 10px;
  background-color: #00d1b2;
  color: #FFF;
  padding: 5px;
  border-radius: 3px;
  cursor: pointer;
}
</style>
