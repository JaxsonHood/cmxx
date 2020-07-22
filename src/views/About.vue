<template>
  <div class="about mx-auto">
    <div class="py-10"></div>

    <v-card
      class="mx-auto"
      max-width="1400"
      outlined
      style="border-radius:32px; padding-top:60px; padding-bottom:65px; padding-left:8px; padding-right:8px;"
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
        >We are a team of Computer Science undergraduate students at Carleton University seeking to help you achieve your digital platform goals. From full-scale applications, to simple blogs we can create a scalable, responsive, and innovative solution to the challenges your business faces. Using up and coming web technologies we can meet the demands of an ever-changing digital landscape.</v-responsive>

        <v-card
          :loading="loading"
          class="mx-auto my-12"
          max-width="1400"
          outlined
          style="border-radius:32px; padding-top:60px; padding-bottom:65px; padding-left:30px; padding-right:30px;"
        >
          <v-container class="text-center">
            <v-row align="center" justify="center">
              <div
                class="transition-swing text-overline"
                style="font-size:55px !important; padding-bottom:40px !important;"
              >Who Are</div>
            </v-row>

            <v-row align="center" justify="center">
              <div
                class="transition-swing text-overline"
                style="font-size:55px !important; padding-bottom:40px !important;"
              >We?</div>
            </v-row>
          </v-container>

          <v-responsive class="mx-auto mb-8" width="56">
            <v-divider class="mb-1"></v-divider>
          </v-responsive>
          <v-row>
            <v-col v-for="(item, i) in section2" :key="i" cols="12" sm="6" style="padding:10px;">
              <v-card>
                <v-avatar size="128">
                  <v-img :src="item.img"></v-img>
                </v-avatar>
                <div class="justify-center text-center"> 
                  <v-card-title class="justify-center text-center">{{item.name}}</v-card-title>
                  <v-card-subtitle class="justify-center text-center">{{item.role}}</v-card-subtitle>
                </div>
                <v-chip-group
                    v-model="selection"
                    active-class="indigo accent-4 white--text"
                    column
                  >
                    <v-chip v-for="(chip, j) in item.skills" :key="j">{{chip}}</v-chip>
              <!-- <v-card>
                <v-list-item>
                  <v-list-item-avatar color="grey"></v-list-item-avatar>
                  <v-list-item-content>
                    <v-list-item-title class="headline">{{item.name}}</v-list-item-title>
                    <v-list-item-subtitle>{{item.role}}</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
                <v-card-text>{{item.desc}}</v-card-text>
                <v-card-text> -->
                  <!-- <v-chip-group
                    v-model="selection"
                    active-class="indigo accent-4 white--text"
                    column
                  >
                    <v-chip v-for="(chip, j) in item.skills" :key="j">{{chip}}</v-chip>
                  </v-chip-group> -->
                <!-- </v-card-text> -->
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
  },
  data() {
    return {
      section2: [
        {
          title: "Who Are",
          subtitle: "We?",
          name: "Cameron Dickie",
          role: "Founder",
          desc: "This is some text that should script itself into the card",
          img: "https://cdn.vuetifyjs.com/images/john.png",
          skills: [
            "skill1",
            "skill2",
            "skill3",
            "skill4",
            "skill5",
            "skill6",
            "skill7"
          ]
        },
        {
          name: "Jaxson Hood",
          role: "Founder",
          desc: "Here is some more text that should script into the card",
          img: "https://cdn.vuetifyjs.com/images/john.png",
          skills: [
            "skill1",
            "skill2",
            "skill3",
            "skill4",
            "skill5",
            "skill6",
            "skill7"
          ]
        }
      ]
    };
  }
};
</script>
