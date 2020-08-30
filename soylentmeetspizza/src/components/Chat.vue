<template>

      

<v-card
    class="mx-auto"
    color="grey lighten-1"
    height="550px"
    width="400px"
  >
  <v-card-title class="headline">Bill Wang</v-card-title>
  <v-divider></v-divider>
  
  <div v-for="text in allTexts" :key="text" style="text-align: right">
      <v-btn style="margin-top:6px; margin-right: 20px;" rounded color="purple lighten-1">{{text}}</v-btn>
  </div>

<v-text-field v-model="text" style="width: 300px; margin-left: 25px; position: absolute; top: 480px;"></v-text-field>
<v-btn v-on:click="sendText" style="position: absolute; top: 500px; left: 330px;" small color="purple lighten-1"><v-icon>mdi-send</v-icon></v-btn>
  
</v-card>

</template>

<script>
export default {
    data() {
        return {
            text: '',
            allTexts: [],
            }
        },
    methods: {
        sendText: function() {
            this.allTexts.push(this.text)
            this.text = '';
    }
    }
    }
</script>
