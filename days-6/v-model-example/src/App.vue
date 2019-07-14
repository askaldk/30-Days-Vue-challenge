<template>
  <div id="app">
    <div class="field">
      <label class="label">Name</label>
      <input type="text" class="input" placeholder="Text input" v-model="name">
    </div>

    <div class="field">
      <label class="label">Subject</label>
      <div class="select">
        <select v-model="subject">
          <option disabled value="">Select dropdown</option>
          <option>Engineering</option>
          <option>Computer Science</option>
          <option>Biology</option>
          <option>Other...</option>
        </select>
      </div>
    </div>

    <div class="field">
      <label class="checkbox">
        <input type="checkbox" v-model="termsAndConditions">
        I agree to the terms and conditions
      </label>
    </div>

    <div class="field2">
      <label class="Yes">
        <input type="radio" v-model="yesOrNo" value="yes">
        Yes
      </label>

      <label class="No">
        <input type="radio" v-model="yesOrNo" value="no">
        No
      </label>
    </div>

    <div class="field">
      <button class="btn btn-primary" id="button" @click="submit">Submit</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      name:'',
      subject:'',
      termsAndConditions:false,
      yesOrNo:'no'
    }
  },
  methods:{
    submit(){
      console.log('name',this.name)
      console.log('subject',this.subject)
      console.log('termsAndConditions',this.termsAndConditions)
      console.log('yesOrNo',this.yesOrNo)
      //ESlint no-console:yes 

    }

  }
}
</script>

<style>
#app{
  max-width:300px ;
  padding-left: 20px;
  padding-top:0px;
}
#app .field {
  display: flex;
  flex-direction: column;
  font-family: cursive;

}

#app .field2 {
  display: flex;
  flex-direction:row;
  font-family: cursive;
  

}
#button{
  max-width:100px ;
}
#app .Yes{
  margin-right: 10px;

}
#app .No{
  margin-right: 10px;

}
input{
  padding:5px;
  margin-top:10px;
  margin-bottom:30px;
  border-color: black;
  border-radius: 4px;
  outline: none;
}
select{
  padding:5px;
  margin-top:10px;
  margin-bottom:30px;
  border-color: black;
  border-radius: 20px;
  outline: none;
}



</style>
