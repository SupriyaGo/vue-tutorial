<template>
  <div>
   <h2 v-bind="$attrs"> Hello {{name}} : {{oName}}</h2>
  </div>
</template>

<script>
  export default {
    name: 'Greet',
    props:['name','oName'],
    inheritAttrs:false
  }
</script>

<style scoped>

</style>