<template>
    <v-container>
        <v-layout row wrap>
           <v-flex xs12 sm6 class="text-xs-center text-sm-right pr-5"> 
             <v-btn large="router" to="/Meetup/meetups" class="primary">Explore Meetups</v-btn>
           </v-flex>
           <v-flex xs12 sm6 class="text-xs-center text-sm-left">
             <v-btn large="router" to="/Meetup/CreateMetups" class="primary">Organize Meetup</v-btn>
           </v-flex>
        </v-layout>
        <v-layout row wrap class="mt-5">
          <v-flex xs12>
            <v-carousel>
              <v-carousel-item
                v-for="meetup in meetups"
                :src="meetup.imageUrl"
                :key="meetup.id">
                <div class="title">
                  {{ meetup.title }}
                </div>
                </v-carousel-item>
            </v-carousel>
          </v-flex>
        </v-layout>
        <v-layout row wrap  class="mt-5">
        <v-flex xs12 class="text-xs-center">
           <p>Join our awesome meetups!</p>
        </v-flex>
       </v-layout>
    </v-container>
</template>

<script>
export default {
    data () {
      return {
        meetups: [
          { imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/4/47/New_york_times_square-terabass.jpg', title: 'Meetup in New York' },
          { imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/7/7a/Paris_-_Blick_vom_gro%C3%9Fen_Triumphbogen.jpg', title: 'Meetup in Paris' }
        ]
      }
    }
  }
</script>

<style scoped>
  .title {
    position: absolute;
    bottom: 50px;
    background-color: rgba(0,0,0,0.5);
    color: white;
    font-size: 2em;
    padding: 20px;
    left: 750px;
  }
</style>
