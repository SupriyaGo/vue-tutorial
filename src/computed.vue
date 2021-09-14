<template>
  <div id="app">
    <h2>{{fullname}}</h2>

  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      fName:'Supriya',
      lName:'Gorai'
    }
  },
  methods:{},
  computed:{
    fullname(){
      return `${this.fName} ${this.lName}`
    }
  }
}
</script>

<style>
#app{
  text-align: center;
}
</style>
