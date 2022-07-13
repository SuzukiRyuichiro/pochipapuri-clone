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
      <h3 class="text-center mb-5">🌸 お天気カメラ 🌸</h3>
      <v-carousel height="144px" hide-delimiter-background hide-delimiters class="mb-5">
        <v-carousel-item v-for="item in items" :key="item.id">
          <div v-html="item.content" class="d-flex justify-center"></div>
        </v-carousel-item>
      </v-carousel>
      <h3 class="text-center mb-5">🌸 最近の投稿 🌸</h3>
      <v-card class="mx-4 mb-10">
        <v-card-subtitle>
          <v-avatar color="primary" class="mr-2" size="24">
            <img src="https://dbsg.aiu.ac.jp/html/img/100000362" alt="Cheong sensei">
          </v-avatar>
          <span class="mr-4">由利本荘市</span>
          <span class="text-caption">8時間前</span>
        </v-card-subtitle>
        <div class="grid">
          <div class="card-category"
            style="background-image: url(https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/breakfast.jpg)">
          </div>

          <div class="card-category"
            style="background-image: url(https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/lunch.jpg)">
          </div>

          <div class="card-category"
            style="background-image: url(https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/dinner.jpg)">
          </div>

          <div class="card-category"
            style="background-image: url(https://images.unsplash.com/photo-1550547660-d9450f859349?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=930&q=80)">
          </div>
        </div>
        <v-card-text>
          イベントを終えて… 【由利本荘市で暮らそう！】 一つの大きなイベントを終えた由利本荘市のナリワイづくり地域おこし協力隊。 少しずつ知り合いも増え、由利本荘市をわたしのまちとして実感してきたようです。
          これからが本番！
        </v-card-text>
      </v-card>

      <h3 class="text-center mb-5">🌸 AKTのtwitter 🌸</h3>
      <v-card class="twitter-container mb-16 mx-2 rounded">
        <a class="twitter-timeline" href="https://twitter.com/akt8_content?ref_src=twsrc%5Etfw">Tweets by
          akt8_content</a>
        <script async type="application/javascript" src="https://platform.twitter.com/widgets.js" charset="utf-8">
        </script>
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

  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 2px;
  }

  .card-category {
    background-size: cover;
    background-position: center;
    height: 180px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-size: 24px;
    font-weight: bold;
    text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
  }

  .twitter-container {
    height: 400px;
    overflow-y: scroll;
  }

</style>
