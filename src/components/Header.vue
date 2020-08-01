<template>
  <v-card
    outlined
    height="74px"
    class="grey lighten-1"
    style="border-radius:15px; margin: auto;"
  >
    <v-toolbar class="elevation-0" height="72px" :dark="false">
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
      </div>

      <v-btn text large href="/home">Home</v-btn>
      <v-btn text large href="/about">About</v-btn>
      <v-btn text large href="/contact">Contact</v-btn>

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

<script>
  export default {
    name: 'Header',
    data () {
      return {}
    },
  }
</script>