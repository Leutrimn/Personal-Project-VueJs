<template>
    <v-container>
        <v-layout row wrap>
           <v-flex xs12 sm6 class="text-xs-center text-sm-right"> 
             <v-btn large="router" to="/Meetup/meetups" class="primary">Explore Meetups</v-btn>
           </v-flex>
           <v-flex xs12 sm6 class="text-xs-center text-sm-left">
             <v-btn large="router" to="/Meetup/CreateMetups" class="primary">Organize Meetup</v-btn>
           </v-flex>
        </v-layout>
        <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
    </v-container>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,

   
  }
}
</script>
