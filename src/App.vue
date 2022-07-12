<template>
  <v-app>
    <v-main>
      <v-card min-height="100px" class="rounded-xl rounded-t-0 text-center mb-8" color="#FBF16A">
        <v-card-title class="justify-center gap-4">
          <span>AKT</span>
          <img :src="require('./assets/pochipa.webp')" alt="Pochipa" id="pochipa">
        </v-card-title>
        <v-card-subtitle>AKTの公式LINEミニアプリ(仮)</v-card-subtitle>
      </v-card>
      <v-card class="mx-4 mb-10">
        <v-card-title class="justify-center">秋田の天気</v-card-title>
      </v-card>
      <h3 class="text-center mb-5">お天気カメラ</h3>
      <v-carousel height="144px" hide-delimiter-background hide-delimiters cycle>
        <v-carousel-item v-for="item in items" :key="item.id">
          <div v-html="item.content" class="d-flex justify-center"></div>
        </v-carousel-item>
      </v-carousel>
      <v-card class="mx-4">
        <v-card-title>秋田市の天気</v-card-title>
        <v-card-subtitle>曇り</v-card-subtitle>
        <v-card-text>28°</v-card-text>
      </v-card>
    </v-main>
    <bottom-nav />
  </v-app>
</template>

<script>
import BottomNav from './components/BottomNav'

export default {
  name: 'App',

  components: {
    BottomNav
  },
  data: () => ({
    items: [{
        id: "1",
        content: '<iframe width="255" height="144" src="https://www.youtube.com/embed/DnFaI4l2bro?controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>'
      },
      {
        id: "2",
        content: '<iframe width="255" height="144" src="https://www.youtube.com/embed/nX4JawVHTO4?controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>'
      }
    ]
  }),
};
</script>

<style lang="scss" scoped>
  .v-main {
    background-color: #F9F5BF;
  }
  #pochipa {
    width: 30px;
    height: 30px;
  }
  .gap-4 {
    gap: 16px;
  }
</style>
