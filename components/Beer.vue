<template>
  <div class="beer">
    <div class="beer__image">
      <img
        :src="beer.image_url"
        :alt="beer.name"
      >
    </div>
    <div class="beer__info">
      <div class="beer__name">
        Name: <span>{{ beer.name }}</span>
      </div>
      <div class="beer__type">
        Type: {{ beer.type }}
      </div>
      <div class="beer__brewer">
        Brewer: {{ beer.brewer }}
      </div>
      <div class="beer__country">
        Country: {{ beer.country }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BeerCard',
  props: {
    beer: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
