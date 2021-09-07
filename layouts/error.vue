<template>
  <div class='container'>
    <p class='error-text'>404</p>
    <div>
      <span>Take me</span>
      <NuxtLink to='/'>Home</NuxtLink>
    </div>
  </div>
</template>
<script>
export default {}
</script>
<style scoped>
.container {
  height: 100vh;
  width: 100vw;
  background-color: aqua;
  text-align: center;
  justify-content: center;
  align-items: center;
}
.error-text {
  display: block;
}
</style>
