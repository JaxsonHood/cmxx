<template>
  <div class="home mx-auto">
    <div class="py-14"></div>

    <v-card
      class="mx-auto"
      max-width="1400"
      outlined
      style="border-radius:32px; padding-top:60px; padding-bottom:65px; padding-left:8px; padding-right:8px;"
    >

      <v-container>
        <v-container class="text-center">
          <h2 class="overline display-2 font-weight-bold mb-3" style="font-size:45px !important;">Services</h2>
        </v-container>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>
        </v-responsive>

        <v-row>
          <v-col
            v-for="(item,i) in section1"
            :key="i"
            cols="12"
            sm="4"
            style="padding:10px;"
          >
              <v-card
                class="mx-auto"
                max-width="375"
                outlined
                style="border-radius:15px; padding:5px;"
              >
                <v-list-item two-line>
                  <v-list-item-content>
                    <div class="overline mb-4">{{item.overline}}</div>
                    <v-list-item-title class="headline mb-1">{{item.heading}}</v-list-item-title>
                    <v-list-item-subtitle class="font-weight-bold">{{item.subhead}}</v-list-item-subtitle>
                  </v-list-item-content>

                  <v-list-item-icon>
                    <v-icon large :color="item.iconColour">{{item.icon}}</v-icon>
                  </v-list-item-icon>

                </v-list-item>

                <v-card-text>
                  {{item.description}}
                </v-card-text>

                <v-card-actions>
                  <v-row
                    align="center"
                    justify="end"
                    style="padding-right:6px;"
                  >
                  <v-btn class="ma-2" outlined :color="item.iconColour">Learn More</v-btn>
                  </v-row>
                  <!-- <v-btn text>Button</v-btn> -->
                </v-card-actions>
              </v-card>
          </v-col>
        </v-row>
      </v-container>
      
    </v-card>

    <div class="py-12"></div>
    <v-card
      :loading="loading"
      class="mx-auto my-12"
      max-width="1400"
      outlined
      style="border-radius:32px; padding-top:60px; padding-bottom:65px; padding-left:8px; padding-right:8px;"
      >
        <v-container class="text-center">
          <h2 class="overline display-2 font-weight-bold mb-3" style="font-size:45px !important;">Who Are We?</h2>
        </v-container>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>
        </v-responsive>
        <v-row>
          <v-col v-for="(item, i) in section2"
          :key="i"
          cols="12"
          sm="6"
          style="padding:10px;">
            <v-card>
              <v-list-item>
              <v-list-item-avatar color="grey"></v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title class="headline">{{item.name}}</v-list-item-title>
                <v-list-item-subtitle>{{item.role}}</v-list-item-subtitle>
              </v-list-item-content>
              </v-list-item>
              <v-card-text>{{item.desc}}</v-card-text>
              <v-card-text>
                <v-chip-group v-model="selection" active-class="indigo accent-4 white--text" column>
                  <v-chip v-for="(chip, j) in item.skills" :key="j">{{chip}}</v-chip>
              </v-chip-group>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
    </v-card>
    
</template>

<script>
// @ is an alias to /src
// import Carousel from '@/components/Carousel.vue'
// import Gallery from '@/components/Gallery.vue'
// import PseudoCarousel from '@/components/PseudoCarousel.vue'
// import Timeline from '@/components/Timeline.vue'


export default {
  name: 'Home',
  components: {
    // Carousel,
    // Gallery,
    // PseudoCarousel,
    // Timeline
  },
  data () {
    return {
      section1:[
        {
          overline: "Fast",
          heading: "Websites",
          subhead: "For any size company.",
          description: "We build fast scalable websites that can integrate well-established standards in design, implimentation, and execution.",
          icon: "web",
          iconColour: "#304FFE"
        },
        {
          overline: "Scalable",
          heading: "Apps",
          subhead: "Delivered to your end user.",
          description: "Using a development tool like Flutter, we can scale your app on android, ios, and even macOS creating a unified experience.",
          icon: "smartphone",
          iconColour: "#FF1744"
        },
        {
          overline: "Smooth",
          heading: "Launch",
          subhead: "Removing stress from the experience.",
          description: "We want your process to be fast and enjoyable with us as we carry the project through development and launch stages.",
          icon: "offline_bolt",
          iconColour: "#00E676"
        }
      ],
      section2:[
        {
          name: "Cameron Dickie",
          role: "Founder",
          desc: "This is some text that should script itself into the card",
          skills: ["skill1", "skill2", "skill3", "skill4", "skill5", "skill6", "skill7"]
        },
        {
          name: "Jaxson Hood",
          role: "Founder",
          desc: "Here is some more text that should script into the card",
          skills: ["skill1", "skill2", "skill3", "skill4", "skill5", "skill6", "skill7"]
        }
      ]
    }
  },
}
</script>
