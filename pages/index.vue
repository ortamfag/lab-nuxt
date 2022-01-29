<template>
  <v-carousel>
    <v-carousel-item
      v-for="(item,i) in articles"
      :key="i"
      :src="`/${item.full_image}`"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default{

    computed:{
      articles(){
        return this.$store.getters["articles/getArticlesSlider"]
      }
    }
  }
</script>