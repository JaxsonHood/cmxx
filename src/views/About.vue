<template>
  <div class="about mx-auto">
    <div class="py-11"></div>

    <v-card
      class="mx-auto"
      max-width="1400"
      outlined
      style="border-radius:32px; padding-top:60px; padding-bottom:65px; padding-left:8px; padding-right:8px;"
    >

      <v-container class="text-center">
        <v-container class="text-center">
          <h2 class="overline display-2 font-weight-bold mb-3" style="font-size:45px !important;">About Us</h2>
        </v-container>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >We are a team of Computer Science undergraduate students at Carleton University seeking to help you achieve your digital platform goals. From full-scale applications, to simple blogs we can create a scalable, responsive, and innovative solution to the challenges your business faces. Using up and coming web technologies we can meet the demands of an ever-changing digital landscape.</v-responsive>

        <v-avatar class="elevation-12 mb-12" size="128">
          <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
        </v-avatar>

        <div></div>
<!-- 
        <v-btn color="grey" href="https://vuetifyjs.com" outlined large>
          <span class="grey--text text--darken-1 font-weight-bold">Vuetify Documentation</span>
        </v-btn> -->
      </v-container>
      
    </v-card>

    <div class="py-12"></div>
    <Card1 />
  </div>
</template>

<script>
// @ is an alias to /src
import Card1 from "@/components/Card1.vue";

export default {
  name: "About",
  components: {
    Card1
  }
};
</script>
