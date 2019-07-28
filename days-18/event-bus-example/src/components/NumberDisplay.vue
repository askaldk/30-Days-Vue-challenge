<template>
  <div>
    <h1>{{numbers}}</h1>
  </div>
</template>
<script>
import { EventBus } from "../EventBus.js";
export default {
  name: "NumberDisplay",
  data() {
    return {
      numbers: [1, 2, 3]
    };
  },
  created() {
    EventBus.$on("NumberAdded", number => {
      this.numbers.push(number);
    });
  }
};
</script>
