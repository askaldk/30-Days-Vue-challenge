<template>
  <div id="app">
    <h1>{{title}}</h1>
    <p v-show="country==='Taiwan'">
      by {{author}} who lives in {{country}}
    </p>
    <p v-show="country==='Japan'">
      by {{author}} who wishes to visit {{country}}
    </p>
    <img :src="image" alt="無法顯示圖片">
    <button v-on:click="changeCountry">changeCountry</button>
  </div>
</template>

<script>


export default {
  name: 'app',
  data(){
    return{
      title:'Hello World!',
      country:'Taiwan',
      author:'Ang Qian',
      image:'./images.jpg'

    }
  },
  methods:{
    changeCountry(){
      if(this.country==='Japan'){
        this.country='Taiwan'
        this.image='./taiwan-banner-sponsor-story.jpg'
      }
      else{
        this.country='Japan'
        this.image='./images.jpg'
      }
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
img{
  height:40vh;
}
button{
  margin-top: 20px;
}
</style>
