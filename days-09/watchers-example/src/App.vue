<template>
  <div id="app">
    <div class="field">
      <label class="label">KM</label>
      <input type="number" v-model="km" class="input" placeholder="input some KM value">
    </div>

    <div class="field">
      <label class="label">M</label>
      <input type="number" v-model="m" class="input" placeholder="input some KM value">
    </div>
  </div>
</template>

<script>


export default {
  name: 'app',
  data(){
    return{
      km:0,
      m:0
    }
  },
  watch:{
    km(){
      this.m=this.km ? this.km*1000 : 0
    },
    m(){
      this.km=this.m ? this.m/1000 : 0
    }
  }

}
</script>

<style>
html,body{
  background-color: blanchedalmond;
}

#app {
  max-width: 300px;
  margin-top:20px;
  margin-left: 10px;

}
</style>
