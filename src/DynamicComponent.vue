<template>
  <div id="app">
    <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>

    <keep-alive>
    <component :is="activeTab"/>
    </keep-alive>
    
  </div>
</template>

<script>
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';
export default {
  name: 'App',
  components:{
    TabA,
    TabB,
    TabC,
  },
  data(){
    return{
      activeTab:'TabA'
    }
  },
  methods:{}
}
</script>

<style>
#app{
  text-align: center;
}
</style>
