<template>
  <div id="app">
    <Card></Card>
     <Card>
      <h2>Card components</h2>
    </Card>
    <Card>
      <img src="https://picsum.photos/200" >
    </Card>
    
    <Card2>
      <template v-slot:header>
        <h3>Header</h3>
      </template>
      <template v-slot:default>
        <img src="https://picsum.photos/200" >
        
      </template>
      <template v-slot:footer>
        <button>update</button>
      </template>
    </Card2>


    <NameList>
      <template v-slot:default="slotProps">
          {{slotProps.firstName}}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
          {{slotProps.firstName}} {{slotProps.lastName}}
      </template>
    </NameList>

  </div>
</template>

<script>
import Card from './components/Card.vue'
import Card2 from './components/Card2.vue'
import NameList from './components/NameList.vue'
export default {
  name: 'App',
  components:{
    Card,
    Card2,
    NameList
  },
  data(){
    return{}
  },
  methods:{}
}
</script>

<style>
#app{
  text-align: center;
}
</style>
