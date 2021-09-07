<template>
  <div class='container'>
    <Nuxt />
  </div>
</template>
<script>
export default {
  head: {
    title: 'Nuxt Mission',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'A nuxt helper' },
    ],
  }
}
</script>
<style scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
