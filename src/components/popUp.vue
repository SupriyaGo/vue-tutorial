<template>
  <div>
   <h2> I am a popup</h2>
    <button @click="$emit('close','Supriya')">Close pop up</button>

  </div>
</template>

<script>
  export default {
    name: 'popUp',
    emits:['close']
  }
</script>

<style scoped>

</style>