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
    v-show="!bill"
  >

    <v-img
      class="white--text align-end"
      height="350px"
      src="https://scontent.xx.fbcdn.net/v/t1.15752-9/118631655_364327857894976_2616781774397461562_n.jpg?_nc_cat=104&_nc_sid=b96e70&_nc_ohc=hCW3_tQm_RIAX_-wLHq&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=ace9dfd087cc5a7c844453934c1715a6&oe=5F6E9760"
    >
      <v-card-title>Bill Wang</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-4">Computer Science Student in Toronto</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Hackathon Enthusiast 💻</div>
      <br>
      <div>Looking for hackathon partners in Toronto. DM if you want to team up, or are looking to connect!</div>
      <br>
      <div>Expertise Area:</div>
      <div>
        <ul>
          <li>Front end</li>
          <li>Back end</li>
          <li>Machine learning</li>
        </ul>
      </div>
        <br>
      <div>
          <v-chip color="purple lighten-1" filter><a href="https://github.com/billwang115">GitHub</a></v-chip>
          <v-chip color="purple lighten-1" filter style="margin-left: 10px; margin-right:10px;"><a href="https://www.linkedin.com/in/billwang115/">LinkedIn</a><br></v-chip>
          <v-chip color="purple lighten-1" filter><a href="https://devpost.com/billwang115">Devpost</a><br></v-chip>
      </div>
    </v-card-text>

    <v-card-actions>
      <v-btn color="purple" text> Send message </v-btn>

      <v-btn color="purple" text> Save </v-btn>
    </v-card-actions>

  </v-card>


  <v-card
    class="mx-auto"
    color="grey darken-3"
    v-show="bill"
  >

    <v-img
      class="white--text align-end"
      height="350px"
      src="https://scontent.xx.fbcdn.net/v/t1.15752-9/118483640_3222722651130832_817294328514744363_n.jpg?_nc_cat=105&_nc_sid=b96e70&_nc_ohc=xTMAhDgMKw0AX-tWmD6&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=12e127535eb14d6db0a7d910dbfcf7be&oe=5F6EFA34"
    >
      <v-card-title>Sujean Pyo</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-4">Criminology Student in Toronto</v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Tech Entrepreneur 💼</div>
      <br>
      <div>Looking for startup partners in Toronto/London area. DM if you are interested!</div>
      <br>
      <div>Expertise Area:</div>
      <div>
        <ul>
          <li>Project Management</li>
          <li>UI Design</li>
        </ul>
      </div>
        <br>
      <div>
          <v-chip color="purple lighten-1" filter><a href="https://github.com/billwang115">GitHub</a></v-chip>
          <v-chip color="purple lighten-1" filter style="margin-left: 10px; margin-right:10px;"><a href="https://www.linkedin.com/in/billwang115/">LinkedIn</a><br></v-chip>
      </div>
    </v-card-text>

    <v-card-actions>
      <v-btn color="purple" text> Send message </v-btn>

      <v-btn color="purple" text> Save </v-btn>
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
