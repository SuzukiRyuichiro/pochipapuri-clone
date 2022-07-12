<template>
  <v-bottom-navigation v-model="value" color="teal" grow hide-on-scroll fixed>
    <v-btn value="home">
      <span>ホーム</span>

      <v-icon>mdi-domain</v-icon>
    </v-btn>
    <v-btn value="recent">
      <span>最新情報</span>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn value="favorites">
      <span>お気に入り</span>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn value="nearby">
      <span>地域情報</span>

      <v-icon>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>
