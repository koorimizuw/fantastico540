<template>
  <div class="title">
    <div class="en">{{en}}</div>
    <div class="jp">{{jp}}</div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: ["en", "jp"]
});
</script>

<style lang="scss" scoped>
.title {
  text-align: center;
  margin-top: 20px;
  padding: 50px;
  line-height: 40px;
  color: #666;
}
.en {
  font-size: 2.5rem;
}
.jp {
  font-size: 2rem;
}
</style>