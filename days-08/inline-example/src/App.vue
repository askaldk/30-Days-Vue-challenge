<template>
  <div id="app">
    <div class="card">
      <header class="card-header card-header-title">
        <span>Original:</span>
        {{message}}
      </header>

      <header class="card-header card-header-title">
        <span>Reversed:</span>
        {{message.split('').reverse().join('')}}
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
