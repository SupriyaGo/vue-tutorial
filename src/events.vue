<template>
  <div id="app">
    <h2>{{ count }}</h2>
    <div>
      <button v-on:click="increment">Increment</button>
      <button v-on:click="decrement">Decrement</button>
      <button @click="incr(2, $event) , message()">Increment by 2</button>
      <button @click="decr(2)">Decrement by 2</button>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      count:0
    }
  },
  methods:{
    increment(event){
      console.log('event:', event)
      this.count += 1;
    },
    decrement(){
      if(this.count !== 0) this.count -= 1;
    },
    incr(a, event){
      console.log('event:', event)
      this.count += a;
    },
    decr(a){
      if(this.count !== 0) this.count -= a;
    },
    message(){
      alert("Success")
    }

  },
}
</script>

<style>
#app{
  text-align: center;
}


</style>
