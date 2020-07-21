<template>
  <v-card
    outlined
    height="80px"
    class="d-flex justify-center"
    min-width="90%"
    style="border-radius:20px;"
  >
    <v-toolbar class="elevation-0" style="padding-top:8px;" max-width="1400px">
      <v-toolbar-items>
        <v-btn icon class="align-self-start" size="28" href="/home">
          <v-icon :color="black">mdi-vector-intersection</v-icon>
        </v-btn>
      </v-toolbar-items>
      <v-toolbar-title>CMXX</v-toolbar-title>

      <v-spacer></v-spacer>
      <div class="text-center">
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