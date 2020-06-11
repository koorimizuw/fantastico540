<template>
  <div>
    <Header :istop="false" />
    <Menu />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Header from "~/components/header/header.vue";
import Menu from "~/components/menu/menu.vue";

export default Vue.extend({
  components: {
    Header,
    Menu
  }
});
</script>

<style lang="scss" scoped>
</style>