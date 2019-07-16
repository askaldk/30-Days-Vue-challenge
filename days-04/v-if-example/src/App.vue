<template>
  <div id="app">
    <h1>{{title}}</h1>
    <p v-if="country === 'Japan'">
      {{author}}  who wishes to visit {{country}}
    </p>
    <p v-if="country === 'Taiwan'">
      {{author}} who lives in {{country}}
    </p>
    <img :src="image" alt="無法顯示圖片">
    <button v-on:click="changeButton">changeButton</button>

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
      image:"./taiwan-banner-sponsor-story.jpg"
    }
  },
  methods:{
    changeButton(){
      if(this.country === 'Taiwan'){
        this.country='Japan';
        this.image='./images.jpg';
      }
      else{
        this.country='Taiwan';
        this.image='./taiwan-banner-sponsor-story.jpg';
      }
      }
    }
  }
</script>

<style>
#app {
  height:100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
img{
  height: 40vh;
}
</style>
