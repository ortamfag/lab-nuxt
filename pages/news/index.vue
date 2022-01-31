<template>
  <div>
    <v-card
      class="mx-auto"
      max-width="344"
      v-for="article in articles"
      :key="article.id"
    >
      <nuxt-link :to="`news/`+article.id">
        <v-img :src="article.preview_image" height="200px"></v-img>

        <v-card-title>
          {{ article.name }}
        </v-card-title>

        <v-card-subtitle>
          {{ article.shortDesc }}
        </v-card-subtitle>
      </nuxt-link>
    </v-card>
  </div>
</template>

<script>
export default {
  computed: {
    articles() {
      return this.$store.getters["articles/getArticles"];
    },
  },
};
</script>

<style>
.v-card__title{
  color: #FFFFFF;
}

.v-application a {
  text-decoration: none;
}

.v-card__subtitle{
  color: #FFFFFF;
}
</style>
