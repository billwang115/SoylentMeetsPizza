<template>

  <div>

    <v-card width="100%" color="purple lighten-1" height="65px" style="margin-bottom:30px"></v-card>

    <div v-show="bottomNav === 'profile'">
      <Profile />
    </div>

    <div v-show="bottomNav === 'swipe'">
      <Swipe />
    </div>

    <div v-show="bottomNav === 'chat'">
      <Chat />
    </div>

  <v-bottom-navigation
    v-model="bottomNav"
    :value="swipe"
    grow
    absolute
    color="purple lighten-1"
  >
    <v-btn value="profile">
      <span>Profile</span>
      <v-icon>mdi-face</v-icon>
    </v-btn>

    <v-btn value="swipe">
      <span>Discover</span>
      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn value="chat">
      <span>Chat</span>
      <v-icon>mdi-chat</v-icon>
    </v-btn>
  </v-bottom-navigation>

  </div>
</template>


<script>
import Profile from './Profile'
import Swipe from './Swipe'
import Chat from './Chat'

  export default {
    components: {
      Profile,
      Swipe,
      Chat
      },
    data () {
      return {
        bottomNav: 'swipe',
      }
    }
  }
</script>
