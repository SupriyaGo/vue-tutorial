<template>
  <div id="card">
    <div id="card-header">
      <slot name="header"></slot>
    </div>
    <div id="card-content">
      <slot></slot>
    </div>
    <div id="card-footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name:'Card2',
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
#card-header{
  text-align: center;
  padding: 5px;
}
#card-footer{
   text-align: center;
  padding: 5px;
}

</style>