<template>
  <v-card
    outlined
    height="74px"
    
    style="border-radius:15px; margin: auto;"
    max-width="1450"
    :dark="true"
  >
    <v-toolbar class="elevation-0" height="72px" :dark="true" max-width="1455">
      <v-toolbar-items>
        <v-btn icon class="align-self-start" size="28" href="/home">
          <v-icon :color="white">mdi-vector-intersection</v-icon>
        </v-btn>
      </v-toolbar-items>
      
      <v-toolbar-title class="d-none d-sm-flex">CMXX</v-toolbar-title>

      <v-spacer></v-spacer>

      <div class="text-center d-none d-md-flex">
        <v-chip
          class="ma-2"
          color="#304FFE"
          outlined
        >
          <v-icon left>web</v-icon>
          Websites
        </v-chip>

        <v-chip
          class="ma-2"
          color="#FF1744"
          outlined
        >
          <v-icon left>smartphone</v-icon>
          Apps
        </v-chip>

        <v-chip
          class="ma-2"
          color="#00E676"
          outlined
        >
          <v-icon left>offline_bolt</v-icon>
          Launch
        </v-chip>
      </div>

      <div style="width:5px;"></div>

      <v-btn id='Home' text large style="border-radius:10px;" :elevation="5" href="/home">Home</v-btn>
      <div style="width:3px;"></div>
      <v-btn id='About' text large style="border-radius:10px;" :elevation="5" href="/about">About</v-btn>
      <div style="width:3px;"></div>
      <v-btn id='Contact' text large style="border-radius:10px;" :elevation="5" href="/contact">Contact</v-btn>

      <!-- <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn> -->

      <!-- <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn> -->
      
    </v-toolbar>
  </v-card>
</template>

<style scoped>
  .in_use {
    display: none;
  }
</style>

<script>
  export default {
    name: 'Header',
    data () {
      return {}
    },
    // watch:{
    //   $route (to, from){
    //       //This changes the link color based on url
    //       document.getElementById(from.name).classList.remove('in_use');
    //       document.getElementById(to.name).classList.add('in_use');
    //   }
    // }
  }
</script>