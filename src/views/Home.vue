<template>
  <div class="home mx-auto" style="background-color:#F5F5F5;">
    <div class="py-11"></div>

    <v-card
      class="mx-auto"
      max-height="700"
      outlined
      style="border-radius:18px;"
      elevation="5"
      max-width="1450"
    >
      <!-- <v-parallax src="https://source.unsplash.com/TTBEwfajRFc/1600x900" height="700"> -->
      <v-parallax src="https://source.unsplash.com/IGtutkXikuc/1600x900" height="700">
          <v-container>
              <v-row>
                <v-col
                  v-for="(item,i) in section3"
                  :key="i"
                  cols="12"
                  sm="12"
                  style="padding:10px;"
                >
                    <v-card
                      :dark="false"
                      class="mx-auto"
                      height="450px"
                      width="600px"
                      outlined
                      style="border-radius:20px; padding:5px; border-color:#263238; border-width:2px;"
                      elevation="5"
                    >

                      <v-row
                          align="center"
                          justify="center"
                          style="padding:35px;"
                        >
                          <div
                            class="transition-swing text-h2"
                            v-text="item.heading"
                            style="font-size:40px !important;"
                          >
                          </div>
                      </v-row>

                       <v-row
                          align="center"
                          justify="center"
                          style="padding-bottom:10px;"
                        >
                          <div
                            class="transition-swing text-overline"
                            v-text="item.subhead"
                            style="font-size:55px !important;"
                          >
                          </div>

                      </v-row>

                      <v-row
                        align="center"
                        justify="center"
                        style="padding-top:30px; padding-left:10px; padding-right:10px;"
                      >
                        <div
                          class="transition-swing text-body-2 text-center"
                          v-text="item.description"
                          style="font-size:16px !important; max-width:370px;"
                        >
                        </div>

                      </v-row>

                      <v-card-actions>
                        <v-row
                          align="center"
                          justify="center"
                          style="padding-top:25px;"
                        >
                        <v-btn href="#" v-scroll-to="'#services'" class="ma-2" outlined :elevation="2" x-large style="border-radius:10px; border-width:1.5px;">Our Services</v-btn>
                        <!-- <v-btn href='/about' class="ma-2" large outlined :color="'#212121'">About Us</v-btn> -->
                        </v-row>
                        <!-- <v-btn text>Button</v-btn> -->
                      </v-card-actions>
                    </v-card>
                </v-col>
              </v-row>
            </v-container>
      </v-parallax>
    </v-card>

    <div class="py-3"></div>

    <v-card
      id="services"
      class="mx-auto"
      outlined
      style="border-radius:18px; padding-top:55px; padding-bottom:60px; padding-left:3px; padding-right:3px;"
      :dark="true"
      elevation="5"
      max-width="1450"
    >

      <v-container>
        <v-container class="text-center">
          <h2 class="overline display-2 font-weight-bold mb-3" style="font-size:45px !important;">We Make</h2>
        </v-container>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>
        </v-responsive>

        <v-row mx-auto align="center" justify="center">
          <v-col
            v-for="(item,i) in section1"
            :key="i"
            cols="12"
            sm="4"
            style="padding:10px; min-width:355px;"
          >
              <v-card
                class="mx-auto"
                max-width="400"
                outlined
                style="border-radius:15px; padding:4px;"
                min-width="325px"
                elevation="10"
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
                  <v-btn class="ma-2" style="border-radius:10px;" :color="item.iconColour">Learn More</v-btn>
                  </v-row>
                  <!-- <v-btn text>Button</v-btn> -->
                </v-card-actions>
              </v-card>
          </v-col>
        </v-row>
      </v-container>
      
    </v-card>

    <div class="py-3"></div>

    <v-card
      class="mx-auto"
      max-height="700"
      outlined
      style="border-radius:18px;"
      elevation="5"
      max-width="1450"
    >
      <!-- <v-parallax src="https://source.unsplash.com/TTBEwfajRFc/1600x900" height="700"> -->
      <v-parallax src="https://source.unsplash.com/CMs6ZGOdyho/1600x900" height="600">
          <v-container>
              <v-row>
                <v-col
                  cols="12"
                  sm="12"
                  style="padding:10px;"
                >
                    <v-card
                      :dark="false"
                      class="mx-auto"
                      height="450px"
                      width="600px"
                      outlined
                      style="border-radius:20px; padding:5px; border-color:#263238; border-width:2px;"
                      elevation="5"
                    >

                      <v-row
                          align="center"
                          justify="center"
                          style="padding-top:60px !important; padding-left:5px; padding-right:5px;"
                        >
                          <div
                            class="transition-swing text-h4 bold"
                            v-text="'Our Team'"
                            style="font-size:40px !important;"
                          >
                          </div>
                      </v-row>

                       <v-row
                          align="center"
                          justify="center"
                        >
                        <div style="max-width:300; padding:10px;">
                          <v-chip-group column>
                            <v-chip
                              class="ma-1"
                              outlined
                            >
                              <v-icon left>perm_identity</v-icon>
                              Cam
                            </v-chip>

                            <v-chip
                              class="ma-1"
                              outlined
                            >
                              <v-icon left>perm_identity</v-icon>
                              Alex
                            </v-chip>

                            <v-chip
                              class="ma-1"
                              outlined
                            >
                              <v-icon left>perm_identity</v-icon>
                              Jaxson
                            </v-chip>

                          </v-chip-group>
                        </div>
                      </v-row>

                      <v-row
                        align="center"
                        justify="center"
                        style="padding-top:20px; padding-left:15px; padding-right:15px;"
                      >
                        <div
                          class="transition-swing text-body-2 text-center"
                          v-text="'Click below to learn more about our team of dedicated keyboard warriors! :)'"
                          style="font-size:16px !important; max-width:370px;"
                        >
                        </div>

                      </v-row>

                      <v-card-actions>
                        <v-row
                          align="center"
                          justify="center"
                          style="padding-top:25px;"
                        >
                          <v-btn href="/about" class="ma-2" outlined :elevation="2" x-large style="border-radius:10px; border-width:1.5px;">See Team</v-btn>                        <!-- <v-btn href='/about' class="ma-2" large outlined :color="'#212121'">About Us</v-btn> -->
                        </v-row>
                        <!-- <v-btn text>Button</v-btn> -->
                      </v-card-actions>
                    </v-card>
                </v-col>
              </v-row>
            </v-container>
      </v-parallax>
    </v-card>


    <div class="py-4"></div>
    
</template>

<style scoped>
  .strokeme {
    color: white;
    text-shadow: -2px -2px 0 #000, 2px -2px 0 #000, -2px 2px 0 #000, 2px 2px 0 #000;
  }
</style>

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
          description: "We build fast, easy to navigate websites that integrate well-established standards in design, implimentation, and execution.",
          icon: "web",
          iconColour: "#304FFE"
        },
        {
          overline: "Scalable",
          heading: "Apps",
          subhead: "Delivered to your end user.",
          description: "Using a development tool like Flutter, we can launch your app on android, ios, and even macOS creating a unified experience.",
          icon: "smartphone",
          iconColour: "#FF1744"
        },
        {
          overline: "Smooth",
          heading: "Launch",
          subhead: "Removing stress from the experience.",
          description: "We want your process to be easy and enjoyable with us as we carry the project through development and launch stages.",
          icon: "offline_bolt",
          iconColour: "#00E676"
        }
      ],
      section3:[
        {
          overline: "Fast",
          heading: "Welcome to",
          subhead: "CMXX",
          description: "We take pride in building beautiful, functional websites & apps that are inspired by modern material design principals.",
          icon: "web",
          iconColour: "#304FFE"
        },
      ],
    }
  },
  methods: {
    scrollToElement(section) {
      const el = this.$el.getElementsByClassName(section)[0];
      if (el) {
        el.scrollToElement();
      }
    }
  }
}
</script>
