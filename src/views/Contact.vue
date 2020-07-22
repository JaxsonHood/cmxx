<template>
  <div class="about mx-auto">
    <div class="py-12"></div>
    <Card1 />
    <div class="py-12"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import Card1 from "@/components/Card1.vue";

export default {
  name: "Contact",
  components: {
    Card1
  }
};
</script>
