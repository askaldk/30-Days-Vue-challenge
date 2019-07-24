<template>
  <div id="app">
    <InLineTemp :message="message" inline-template>
      <div class="card">
        <header class="card-header card-header-title">{{ message }}</header>
      </div>
    </InLineTemp>
  </div>
</template>

<script>
import InLineTemp from "./components/InLineTemp";
export default {
  name: "app",
  data() {
    return {
      message: "Greetings!"
    };
  },
  components: {
    InLineTemp
  }
};
</script>

<style>
html, body {
  height: 100%;
  padding-top: 10px;
  background: #e6ecf1;
}

#app {
  height: 100%;
  max-width: 400px;
  padding-left: 20px;
  padding-top: 10px;
}

header span {
  font-weight: 400;
  padding-right: 5px;
}

header .button {
  margin: 0 auto;
}
</style>
