<template>
  <div id="app">
    <h2>name : {{firstname}}</h2>
    <h2>name : {{state.lastname}}</h2>
  </div>
</template>

<script>
import {ref,reactive} from 'vue';
export default {
  name: 'App',
  setup(){
    const firstname = ref('Supu');

    const state = reactive({
      lastname:'Gorai',
    });

    return{
      firstname,
      state
    }
  }
}
</script>

<style>
#app{
  text-align: center;
}
</style>
