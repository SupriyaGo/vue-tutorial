<template>
  <div id="card">
    <!-- {{title}} -->
    <slot>Default slot value</slot>
  </div>
</template>

<script>
  export default {
    name:'Card',
    props:['title']
  }
</script>

<style scoped>
#card{
  padding: 1em 2em;
  border: 1px solid #ccc;
  margin: 2em;
  transition: 0.3s;
}
#card:hover{
  background-color: #eee;
}

</style>