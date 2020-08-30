<template>

  <div>

    <v-card width="100%" color="purple lighten-1" height="65px" style="margin-bottom:30px; text-align: center;">
      <v-img height="65px" width="50px"
        src="https://scontent.xx.fbcdn.net/v/t1.15752-9/118645847_345927646540309_2607116623102179277_n.png?_nc_cat=109&_nc_sid=b96e70&_nc_ohc=C72hF17o9i0AX8TsJgD&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=1de94888c58a5b5f391c06c632bc1e6f&oe=5F716EB2"
      >
      </v-img>
    </v-card>

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
