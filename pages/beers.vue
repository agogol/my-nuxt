<template>
  <div class="container">
    <p v-if="$fetchState.pending">
      Fetching beers...
    </p>
    <p v-else-if="$fetchState.error">
      An error occurred :(
    </p>
    <div
      v-else
      class="beers"
    >
      <Beer
        v-for="beer in beers"
        :key="beer.beer_id"
        :beer="beer"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'BeersPage',
  data() {
    return {
      beers: []
    }
  },
  async fetch() {
    this.beers = await fetch(
      'https://api.nuxtjs.dev/beers'
    ).then(res => res.json())
  }
}
</script>
