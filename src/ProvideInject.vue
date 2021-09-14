<template>
  <div id="app">
    <h2>App Component name: {{name}}</h2>
    <CompA/>
  </div>
</template>

<script>
import CompA from './components/CompA.vue'
export default {
  name: 'App',
  components:{
    CompA,
  },
  data(){
    return{
      name:'Supu',
    }
  },
  provide(){
    return{
      userName: this.name,
      address:'Mekhliganj'
    }
  }
}
</script>

<style>
#app{
  text-align: center;
}
</style>
