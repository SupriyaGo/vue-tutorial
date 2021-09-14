<template>
  <div id="app">
    <h2>Volume: {{volume}}</h2>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Increase</button>
    </div>

  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      volume:0
    }
  },
  methods:{},
  computed:{},
  watch:{
    volume(newValue, oldValue){
      if(newValue > oldValue && newValue === 16){
        alert("High volume")
      }
    }
  }
}
</script>

<style>
#app{
  text-align: center;
}
</style>
