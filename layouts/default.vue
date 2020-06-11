<template>
  <div>
    <div class="container">
      <nuxt />
      <Footer />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import "assets/html5reset-1.6.1.css";
import Footer from "~/components/footer.vue";

export default Vue.extend({
  components: {
    Footer
  }
});
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.footer {
  flex: 1;
}
</style>