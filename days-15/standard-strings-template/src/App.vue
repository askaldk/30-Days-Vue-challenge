<template>
  <div id="app">
    <SingleLineTemplate :message="message"></SingleLineTemplate>
  </div>
</template>

<script>
import SingleLineTemplate from './components/SingleLineTemplate'
export default {
  name: 'app',
  data(){
    return{
      message:'Greetings!'

    }
  },
  components:{
    SingleLineTemplate
  }
}
</script>

<style>
html, body {
  height: 100%;
  padding-top: 10px;
  background: #e6ecf1;
}

#app {
  height: 100%;
  max-width: 400px;
  padding-left: 20px;
  padding-top: 10px;
}

header span {
  font-weight: 400;
  padding-right: 5px;
}

header .button {
  margin: 0 auto;
}
</style>
