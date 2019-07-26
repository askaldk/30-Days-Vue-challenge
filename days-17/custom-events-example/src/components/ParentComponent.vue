<template>
  <div>
    <ChildComponent :numbers="numbers" @NumberAdded="numbers.push($event)"></ChildComponent>
  </div>
</template>
<script>
import ChildComponent from "./ChildComponent";
export default {
  data() {
    return {
      numbers: [1, 2, 3]
    };
  },
  components: {
    ChildComponent
  } 
};
</script>

