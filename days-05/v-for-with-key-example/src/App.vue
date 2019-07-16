<template>
  <div id="app">
    <ul>
      <li v-for="number in numbers" :key="number.id">
        <p>{{number.value}}</p>
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
      numbers:[
      {id:1,value:1},
      {id:2,value:10},
      {id:3,value:100},
      {id:4,value:1000},
      {id:5,value:10000}
      ]
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
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  
}
ul{
  list-style: none;
}
</style>
