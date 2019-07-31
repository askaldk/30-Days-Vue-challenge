<template>
  <h2>{{storeState.numbers}}</h2>
</template>
<script>
import { store } from "../store";
export default {
  name: "NumberDisplay",
  data() {
    return {
      storeState: store.state
    };
  }
};
</script>
