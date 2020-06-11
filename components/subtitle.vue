<template>
  <div class="title">{{text}}</div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: ["text"]
});
</script>

<style lang="scss" scoped>
.title {
  font-size: 1.8rem;
  &::after {
    content: "";
    width: 100%;
    height: 1px;
    background-color: #ccc;
    display: block;
    margin: 5px 0 10px;
  }
}
</style>