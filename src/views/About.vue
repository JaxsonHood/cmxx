<template>
  <div class="about mx-auto">
    <div class="py-10"></div>

    <v-card
      class="mx-auto"
      outlined
      style="border-radius:18px; padding-top:60px; padding-bottom:65px; padding-left:8px; padding-right:8px;"
      :dark="true"
    >
      <v-container class="text-center">
        <v-container class="text-center">
          <h2
            class="overline display-2 font-weight-bold mb-3"
            style="font-size:45px !important;"
          >About Us</h2>
        </v-container>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >We are a team of Computer Scientists seeking to help you achieve your digital platform goals. From full-scale applications, to simple blogs. We can create a scalable, responsive, and innovative solution to the challenges your business faces. Using up and coming web technologies we can meet the demands of an ever-changing online landscape.</v-responsive>

        <v-card
          :dark="false"
          class="mx-auto"
          outlined
          style="border-radius:20px;"
          color="grey lighten-3"
        >
          <v-row>
            <v-col
              v-for="(item,i) in theboys"
              :key="i"
              cols="12"
              sm="4"
              style="padding:10px;"
            >
              <v-card
                class="mx-auto my-12"
                style="border-radius:20px; padding:5px;"
                max-width="330"
                :dark="true"
                outlined
                elevation="5"
              >

                <v-row align="center" justify="center" style="height:210px; padding-top:15px;">
                  <v-avatar color="orange" size="170">
                    <!-- <span class="white--text headline">170</span> -->
                    <v-img
                      height="200"
                      v-bind:src="require('../assets/' + item.img)"
                    ></v-img>
                  </v-avatar>
                </v-row>

                <v-card-title class="justify-center overline" style="font-size:23px !important;">{{item.name}}</v-card-title>
                <v-card-subtitle><div class="text-center">{{item.role}}</div></v-card-subtitle>
                <v-card-text>
                  <div style="color:#EEEEEE;" class="text-center">{{item.writeup}}</div>
                </v-card-text>

                <v-divider class="mx-4"></v-divider>

                <v-card-title><div style="color:#757575;">SPECIALTIES:</div></v-card-title>

                <v-card-text>
                  <v-chip-group
                    column
                  >
                    <v-chip 
                      v-for="(skill,j) in item.skills"
                      :key="j"
                      :color=skill.color
                      outlined
                    >{{skill.title}}</v-chip>
                  </v-chip-group>
                </v-card-text>

                <v-card-actions>
                  <!-- <v-btn
                    color="deep-purple lighten-2"
                    text
                    @click="reserve"
                  >
                    Reserve
                  </v-btn> -->
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-card>

        <div></div>
        <!-- 
        <v-btn color="grey" href="https://vuetifyjs.com" outlined large>
          <span class="grey--text text--darken-1 font-weight-bold">Vuetify Documentation</span>
        </v-btn>-->
      </v-container>
    </v-card>

    <div class="py-12"></div>
    
  </div>
</template>

<script>
// @ is an alias to /src
// import Card1 from "@/components/Card1.vue";

export default {
  name: "About",
  components: {
    // Card1
  },
  data() {
    return {
      theboys: [
        {
          name: "Jaxson Hood",
          role: "UX Designer / Software Developer",
          writeup: "As a team member at CMXX I believe in creating products that elevate the client experience, and an enviroment that pushes the team to new heights.",
          img: "jaxson.jpeg",
          skills: [
            {
              title: "UI Conception",
              color:"light-blue accent-3"
            },
            {
              title: "Clean Design",
              color:"green accent-3"
            },
            {
              title: "Optimization",
              color:"red accent-3"
            },
            {
              title: "Proj. Organization",
              color:"amber accent-3"
            },
          ]
        },
        {
          name: "Cameron Dickie",
          role: "UI Designer / Software Developer",
          writeup: "As a team member at CMXX I believe in creating products that elevate the client experience, and an enviroment that pushes the team to new heights.",
          img: "placeholder-profile.jpg",
          skills: [
            {
              title: "UI Conception",
              color:"light-blue accent-3"
            },
            {
              title: "Clean Design",
              color:"green accent-3"
            },
            {
              title: "Optimization",
              color:"red accent-3"
            },
            {
              title: "Proj. Organization",
              color:"amber accent-3"
            },
          ]
        },
        {
          name: "Alex Collins",
          role: "Business Lead / Product Consultant",
          writeup: "As a team member at CMXX I believe in creating products that elevate the client experience, and an enviroment that pushes the team to new heights.",
          img: "placeholder-profile.jpg",
          skills: [
            {
              title: "UI Conception",
              color:"light-blue accent-3"
            },
            {
              title: "Clean Design",
              color:"green accent-3"
            },
            {
              title: "Optimization",
              color:"red accent-3"
            },
            {
              title: "Proj. Organization",
              color:"amber accent-3"
            },
          ]
        },
      ]
    };
  }
};
</script>
