<template>
  <div id="app">
    <h2>App Component {{name}}</h2>
    <button @click="visible = true">Open pop up</button>
    <PopUp v-show="visible" @close="closePopUp"/>
  </div>
</template>

<script>
import PopUp from './components/popUp.vue'
export default {
  name: 'App',
  components:{
    PopUp,
  },
  data(){
    return{
      name:'Supu',
      visible:false
    }
  },
  methods:{
    closePopUp(nameArg){
      this.visible = false;
      this.name = nameArg
    }
  }
}
</script>

<style>
#app{
  text-align: center;
}
</style>
