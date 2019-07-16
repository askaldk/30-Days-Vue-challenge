<template>
  <div id="app">
    <h1>{{title}}</h1>
    <p>By {{author}} from {{country}}</p>
    <button v-on:click="changeButton">{{ buttonTag  }}</button>

  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return{
      title:"Hello World!",
      author:"Ang Qian",
      country:"Taiwan",
      buttonTag: "Hello World!"
    }
  },

  methods:{
  changeButton(){
    if(this.buttonTag === 'Hello World!'){
      this.buttonTag="What's up!";
      }else{
      this.buttonTag= "Hello World!";
      }
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

}
h1{
  margin-top: 0;
}
p{
  margin-top:0;
}
</style>
