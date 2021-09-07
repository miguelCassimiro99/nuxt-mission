<template>
  <div>
    <div class="navigation-links">
      <NuxtLink to='/'>Home</NuxtLink>
      <NuxtLink to='/about'>About</NuxtLink>
    </div>
    <div class='container'>
      <Nuxt />
    </div>
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
.navigation-links {
  display: block;
  text-align: center;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
