<template>
  <v-app>
    <div class="fixedHead">
      <Header/>
    </div>
    <v-content>
      <v-container fluid>
        <router-view />
      </v-container>
    </v-content>
  <Footer/>
  </v-app>
</template>

<style scoped>
  .fixedHead {
    position:fixed;
    width:100%;
    z-index:100;
    padding:8px;
  }
</style>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: "App",
  components: {
    Header,
    Footer
  },
  data() {
    return {
      //
    };
  }
};
</script>