<template>
  <div >

    <h2 v-for="name in list" :key="name.fname">
       <!-- {{name.fName}} {{name.lName}} -->
      <slot :firstName="name.fName" :lastName='name.lName'></slot>
    </h2>
   
  </div>
</template>

<script>
  export default {
    name:'NameList',
    data(){
      return{
        list:[
          {
            fName:'Bruce',
            lName:'Wayne'
          },
          {
            fName:'Clark',
            lName:'Kent'
          },
          {
            fName:'Princes',
            lName:'Diana'
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>