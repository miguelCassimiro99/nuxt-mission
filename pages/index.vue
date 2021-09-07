<template>
  <section class="container">
    <div>
      <NuxtLogo />
      <h1 class="title">Nuxt Mission</h1>
      <button @click='showPlanets'>Show planets</button>
      <div v-if="show">
        <LazyPlanetList />
      </div>

    </div>
  </section>

</template>
<script>
import NuxtLogo from '~/components/NuxtLogo'
export default {
  components: { NuxtLogo },
  data() {
    return {
      show: false,
    }
  },
  methods: {
    showPlanets() {
      this.show = !this.show;
    }
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
