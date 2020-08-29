<template>

  <div>

    <div v-show="bottomNav === 'profile'">
1
    </div>

    <div v-show="bottomNav === 'swipe'">
2
    </div>

    <div v-show="bottomNav === 'chat'">
3
    </div>

  <v-bottom-navigation
    v-model="bottomNav"
  >
    <v-btn value="profile">
      <span>Recent</span>
      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn value="swipe">
      <span>Favorites</span>
      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn value="chat">
      <span>Nearby</span>
      <v-icon>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>

  </div>
</template>


<script>
  export default {
    data () {
      return {
        bottomNav: 'swipe',
      }
    },
  }
</script>
