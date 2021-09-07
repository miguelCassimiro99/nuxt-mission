<template>
  <section>
    <NuxtLink to='/'>Home</NuxtLink>
    <div class="container">
      <div>
        <img :src="planet.image" alt="" />
        <h1 class="title">{{ planet.title }}</h1>
      </div>
      <PlanetList />
      <div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ params }) {
    const planet = await fetch(
      `https://api.nuxtjs.dev/planets/${params.slug}`
    ).then((res) => {
      if(res.ok) {
        return res.json()
      }
      throw new Error(res.status)
    })
    return { planet }
  },

  head() {
    return {
      title: this.planet.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.planet.description
        }
      ],
      link: [
        {
          hid: 'canonical',
          rel: 'canonical',
          href: `https://jamstack-explorers-nuxt-mission/${this.$route.params.slug}`
        }
      ]
    }
  },

}
</script>
<style scoped>

h1 {
  font-family: Nunito, sans-serif;
}

img {
  height: 80px;
  width: auto;
  object-fit: cover;
}

</style>
