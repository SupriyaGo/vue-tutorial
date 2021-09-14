<template>
  <div id="app">
    <Greet name="Bruce" oName="batman" id="my-greet"/>
    <Greet :name='name' :oName='orgName'/>
  </div>
</template>

<script>
import Greet from './components/Greet.vue'
export default {
  name: 'App',
  components:{
    Greet,
  },
  data(){
    return{
      name:'Supu',
      orgName:'Supriya'
    }
  },
  methods:{},
  computed:{},
  watch:{}
}
</script>

<style>
#app{
  text-align: center;
}
</style>
