<template>
  <div>
    <h1>{{numbers}}</h1>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  props: {
    numbers: Array
  }
};
</script>
