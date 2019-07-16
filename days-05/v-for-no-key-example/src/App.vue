<template>
  <div id="app">
    <ul>
      <li v-for="number in numbers">
        <!--eslint 沒有key會噴錯-->
        <p>{{number}}</p>
        <input type="text" placeholder="type something...">

      </li>
    </ul>
    <button @click="shuffle">Shuffle!</button>
    
  </div>
  
</template>

<script>
import _ from 'lodash'

export default {
  name: 'app',
  data(){
    return{
      numbers:[1,10,100,1000,10000]

    }
  },
  methods:{
    shuffle(){
      this.numbers=_.shuffle(this.numbers)

   }
 }
  
}
</script>

<style>
#app {
  height: 100vh;
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
}
ul{
  list-style: none;
}
input{
  padding: 5px;
}
p{
  font-size: 18px;
}
</style>
