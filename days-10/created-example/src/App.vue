<template>
  <div id="app">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title">
          {{name}}
        </p>
      </header>
    </div>

    <div class="card-content">
      <div class="content">
        <p>{{company.name}}</p>
        <p>{{company.catchPhrase}}</p>
      </div>
    </div>

    <div class="card-footer">
      <a href="#" class="card-footer-item">{{email}}</a>
    </div>
  </div>
</template>

<script>
import axios  from 'axios'
export default {
  name: 'app',
  data(){
    return{
      name:'Loading...',
      email:'Loading...',
      company:{
        name:'Loading...',
        catchPhrase:'Loading...'
      }
    }
  },
  created(){
    axios.get(
      'https://jsonplaceholder.typicode.com/users'
    ).then((response)=>{
      const data = response.data
      const randomUser =response.data[
        Math.floor(Math.random()*data.length)
      ]

      this.name = randomUser.name
      this.email = randomUser.email
      this.company.name = randomUser.company.name
      this.company.catchPhrase =randomUser.company.catchPhrase
    })
  }
}
</script>

<style>
html,body{
  background-color: beige;
}
#app {
  margin-top: 20px;
  margin-left: 10px;
  max-width: 300px;
}
</style>
