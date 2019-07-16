<template>
  <div id="app">
    <h1>{{fish}}</h1>
    <p>{{introduce}}</p>
  </div>
</template>

<script>


export default {
  name: 'app',
  data(){
    return{
      fish:"Hello World!",
      introduce:"By Ang Qian who lives in Taiwan"

    }
  }
  
}
</script>

<style>

html,body{
  background-color:darkcyan;
  height: 100%;
}
#app {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
h1 {
  margin-top: 0;
}
p{
  margin-top: 0;
  font-size:18px;
}
</style>
