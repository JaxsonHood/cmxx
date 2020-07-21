<template>
  <div class="home mx-auto">
    <div class="py-12"></div>

    <v-card
      class="mx-auto"
      max-width="1400"
      max-height="750"
      outlined
      style="border-radius:32px;"
    >
      <v-parallax src="https://source.unsplash.com/Im7lZjxeLhg/1600x900" height="800">

      
      </v-parallax>
    </v-card>

    <div class="py-12"></div>

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
    <!-- <Chart/>
    <div style="height:20px;"></div>
    <Form/>
    <div style="height:20px;"></div>
    <Blog/>
    <div style="height:40px;"></div>
    <div style="height:40px;"></div> -->
  <!-- <div class="mx-auto" style="max-width:1000px;">
    <PseudoCarousel/>
    <Timeline/>
    <Gallery/>
    <Carousel/>
  </div> -->
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
      ]
    }
  },
}
</script>
