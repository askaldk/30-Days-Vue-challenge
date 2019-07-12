<template>
  <div id="app">
    <h1>{{title}}</h1>
    <p>{{alertMessage}}</p>
    <button v-on:click="changeButton">changeButton</button>
    <button v-on:dblclick="changeButton">double click to changeButton</button>
    <input v-on:keyup="alertMessageChange" placeholder="Typesomething">
    <input v-on:keyup.enter="alertEnterChange" placeholder="Type and release something">
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return{
      title:"Hello World!",
      alertMessage:""
    }
  },
  methods:{
    changeButton(){
      this.title=this.title==='Hello World!'?
      this.title="What's up!":
      this.title="Hello World!";

    },
    alertMessageChange(){
      this.alertMessage='You typed something!';

    },
    alertEnterChange(){
      this.alertMessage='You typed and pressed Enter!';
    }
  }
  
}
</script>

<style>
#app {
  height: 100vh;
  display: flex;
  flex-direction:column;
  justify-content: center;
  align-items: center; 
}
button{
  margin-top: 20px;
}
input{
  margin-top: 20px;
}
</style>
