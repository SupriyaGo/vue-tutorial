<template>
  <div>
    <h2>Component C</h2>
    <h2>Component C User name {{userName}} from {{address}}</h2>
  </div>
</template>

<script>
  export default {
    name: 'CompC',
    inject:['userName', 'address']
  }
</script>

<style scoped>

</style>