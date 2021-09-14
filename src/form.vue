<template>
  <div id="app">
    <p>{{ JSON.stringify(formValues,null, 2) }}</p>


    <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" name="name" id="name" v-model.trim.lazy="formValues.name">
    </div>
    <div>
      <label for="age">Age</label>
      <input @keyup.enter="submitForm" type="text" name="age" id="age" v-model.number="formValues.age">
    </div>
    <div>
      <label for="summery">Summery</label>
      <textarea name="summery" id="summery" cols="30" rows="3" v-model="formValues.summery"></textarea>
    </div>
    
    <div>
      <label for="country">Country</label>
      <select name="country" id="country" v-model="formValues.country">
        <option value="">Select country</option>
        <option value="India">India</option>
        <option value="Russia">Russia</option>
        <option value="Canada">Canada</option>
      </select>
    </div>

     <div>
      <label for="location">Location</label>
      <select name="location" id="location" multiple v-model="formValues.location">
        <option value="India">India</option>
        <option value="Russia">Russia</option>
        <option value="Canada">Canada</option>
      </select>
    </div>

    <div>
      <label for="location">Open to work</label>
      <input type="checkbox" name="remote-work" id="remote-work" v-model="formValues.remoteWork" true-value="yes" false-value="no">
    </div>
    <div>
      <label for="exp">Years of experience</label>
      <input type="radio" name="exp" id="exp" value="0-2" v-model="formValues.exp" >
      <label for="0-2">0-2</label>
      <input type="radio" name="exp" id="exp" value="3-5" v-model="formValues.exp" >
      <label for="3-5">3-5</label>
      <input type="radio" name="exp" id="exp" value="5+" v-model="formValues.exp" >
      <label for="5+">5+</label>
    </div>
    <button>Submit</button>

    </form>

    <h2 v-once>{{name}}</h2>
    <h2 v-pre>{{name}}</h2>

  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      formValues:{
        name:"",
        summery:"",
        country:"",
        location:[],
        remoteWork:'no',
        exp:'',
        age:null
      }
    }
  },
  methods:{
    submitForm(){
      // e.preventDefault();
      console.log("form values", this.formValues);
    }
  },
}
</script>

<style>
#app{
  text-align: center;
}
</style>
