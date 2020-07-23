<template>
  <v-footer
    :dark="false"
    padless
    class="d-flex justify-center"
    style="margin: auto;"
  >
    <v-card
      :dark="true"
      flat
      tile
      max-width="1400px"
      class="lighten-1 text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="pt-0">
        To get in touch, visit our contact page! We believe in producing a good product for value because we know how frustrating it is to have expectation not met, thats why we use the best technologies that are required for each unique project!
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="">
        {{ new Date().getFullYear() }} — <strong>CMXX&trade;</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    name:"Footer",
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>

