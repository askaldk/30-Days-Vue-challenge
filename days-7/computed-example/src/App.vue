<template>
  <div id="app">
    <div class="card colums">
      <header class="card-header card-header-title">
        <span>Original:</span>
        {{message}}
      </header>

      <header class="card-header card-header-title">
        <span>Reversed:</span>
        {{reverseMessage}}
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
  computed:{
    reverseMessage(){
      return this.message.split('').reverse().join('')
    }
  }
  
}
</script>

<style>
#app {
  max-width: 300px;
  padding-left:20px;
  padding-top:10px;
  
}

header span{
  font-weight:400;
}

</style>
