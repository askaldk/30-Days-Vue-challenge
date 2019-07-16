<template>
  <div id="app">
    <h1>{{title}}</h1>
    <p>By{{author}}from{{country}}</p>
    <button  v-on:click="changeButton">
      changeButton
    </button>
      
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return{
      title:"Hello World",
      author:" Ang Qian ",
      country:" Taiwan"
    }
  },
  methods:{
    changeButton(){
      this.title = this.title === "Hello World" ?
       "What's wrong":
       "Hello World";
    }
  }
}
</script>

<style>
html,body{
  background-color: aquamarine;

}
#app {
  height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;

}
h1{
  margin-top: 0;

}
p{
  margin-top: 0;
  font-size: 18px;
}
</style>
