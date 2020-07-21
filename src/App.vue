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
  </v-app>
</template>

<style scoped>
  .fixedHead {
    position:fixed;
    top:0;
    width:100%;
    z-index:100;
  }
</style>

<script>
import Header from '@/components/Header.vue'

export default {
  name: "App",
  components: {
    Header
  },
  data() {
    return {
      //
    };
  }
};
</script>