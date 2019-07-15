<template>
  <div id="app">
    <div class="field">
      <label class="label">KM</label>
      <input v-model="km" class="input" type="number" placeholder="Tyep a length in KM!">
    </div>
    
    <div class="field">
      <label class="label">M</label>
      <input v-model="m" class="input" type="number" placeholder="Type a length in M!">
    </div>
  
  </div>
</template>

<script>


export default {
  name: 'app',
  data(){
    return{
      km:0
    }
  },
  computed:{
    m:{
      get(){
        return this.km*1000
      },
      set(newValue){
        this.km = newValue/1000
      }
    }
  }
 
}
</script>

<style>
html,body{
  background-color:aliceblue;
}
#app {
  
 height: 100vh;
 display: flex;
 flex-direction: column;
 max-width: 300px;
 margin-top:20px;
 margin-left: 10px;
}

</style>
