<template>
  <v-app style="background-color:#F5F5F5;">
    <div class="fixedHead">
      <Header/>
    </div>
    <v-main>
      <v-container fluid>
        <router-view />
      </v-container>
    </v-main>
  <Footer/>
  </v-app>
</template>

<style scoped>
  .fixedHead {
    position:fixed;
    width:100%;
    z-index:100;
    padding:8px;
    padding-top: 10px !important;
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