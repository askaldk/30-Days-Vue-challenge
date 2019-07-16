<template>
  <div id="app">
    <div class="card">
      <header class="card-header card-header-title">
        <span>Original:</span>
        {{message}}        
      </header>

      <header class="card-header card-header-title">
        <span>Reverse:</span>
        {{reverseMessage(message)}}

      </header>
    </div>
  </div>
</template>

<script>


export default {
  name: 'app',
  data(){
    return{
      message:'Greetings!'
    }
  },
  methods:{
    reverseMessage(String){
      return String.split('').reverse().join('')
    }
  }
}
</script>

<style>
#app {
  max-width: 300px;
  margin-top:20px;
  margin-left: 10px; 
}
header span{
  font-weight: 400;
}
</style>
