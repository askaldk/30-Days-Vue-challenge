<template>
  <div id="app">
    <ul>
      <li v-for="number in numbers" >{{number}}</li>
      <!--eslint 沒有key會噴錯-->
    </ul>
    
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return{
      numbers:[1,10,100,1000,10000]
    }
  }
  
}
</script>

<style>
#app {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;


}
ul{
  list-style: none;
  font-size: 30px;
}
</style>
