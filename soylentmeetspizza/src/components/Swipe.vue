<template>
<div>

    <v-btn v-on:click="swap()" style="position: absolute; top: 400px; left: 1000px;" color="purple lighten-1"><v-icon>mdi-arrow-right</v-icon></v-btn>
    <v-btn v-on:click="swap()" style="position: absolute; top: 400px; left: 450px;" color="purple lighten-1"><v-icon>mdi-arrow-left</v-icon></v-btn>

<v-container
      id="scroll-target"
      style="max-height: 550px; max-width: 400px; padding-top: 0; padding-bottom: 0;"
      class="overflow-y-auto"
    >
      <v-row
        align="center"
        justify="center"
      >
      

<v-card
    class="mx-auto"
    color="grey darken-3"
    v-show="bill"
  >

    <v-img
      class="white--text align-end"
      height="350px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>Bill Wang</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-4">Computer Science Student in Toronto</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Hackathon enthusiast 💻</div>
      <div>Looking for hackathon partners in Toronto. DM if you want to team up, or are looking to connect!</div>
        <br>
      <div>
          <v-chip color="purple lighten-1" filter><a href="https://github.com/billwang115">GitHub</a></v-chip>
          <v-chip color="purple lighten-1" filter style="margin-left: 10px; margin-right:10px;"><a href="https://www.linkedin.com/in/billwang115/">LinkedIn</a><br></v-chip>
          <v-chip color="purple lighten-1" filter><a href="https://devpost.com/billwang115">Devpost</a><br></v-chip>
      </div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="purple"
        text
      >
        Send message
      </v-btn>

      <v-btn
        color="purple"
        text
      >
        Save
      </v-btn>

    </v-card-actions>

  </v-card>


  <v-card
    class="mx-auto"
    color="grey darken-3"
    v-show="!bill"
  >

    <v-img
      class="white--text align-end"
      height="350px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>Sujean Pyo</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-4">Criminology Student in Toronto</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Nerd</div>
      <div>Am nerd</div>
        <br>
      <div>
          <v-chip color="purple lighten-1" filter><a href="https://www.linkedin.com/in/billwang115/">LinkedIn</a><br></v-chip>
      </div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="purple"
        text
      >
        Send message
      </v-btn>

      <v-btn
        color="purple"
        text
      >
        Save
      </v-btn>

    </v-card-actions>

  </v-card>

  </v-row>
    </v-container>

</div>
</template>

<script>
export default {
    data () {
      return {
          bill: true
      }
    },
    methods: {
        swap: function() {
            this.bill = !this.bill
            }
        }
    }
</script>
