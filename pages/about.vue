<template>
  <div>
    <h1>About</h1>
    <p v-if="$nuxt.isOffline">
      oops, you are offline
    </p>
    <p v-if="$nuxt.isOnline">
      yeaahhh
    </p>
    <NuxtLink to="/">
      Home
    </NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>

<style scoped>

</style>
