<template>
  <div id="app">
    <h1>{{title}}</h1>
    <p>By {{author}} who lives {{country}}</p>
    <img :src="image" alt="無法顯示圖片">
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
  }
}
</script>

<style>
html,body{
  background-color: azure;
}
#app {
  align-items: center;
  height:100vh ;
  justify-content: center;
  display: flex;
  flex-direction: column;

}
img{
  height: 40vh;
  width: 40vw;
}
</style>
