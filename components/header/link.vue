<template>
  <nuxt-link :to="to" class="link">
    <div class="text">
      <div class="en">{{en}}</div>
      <div class="jp">{{jp}}</div>
    </div>
  </nuxt-link>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: ["istop", "to", "en", "jp"]
});
</script>

<style lang="scss" scoped>
.link {
  text-align: center;
  display: flex;
  text-decoration: none;
  height: 100%;
  width: 150px;
  &:hover {
    transition: 0.5s;
    background-color: rgba(255, 255, 255, 0.5);
  }
}

.text {
  text-align: center;
  width: 100%;
}

.en {
  color: #9e9764;
  font-size: 1.3rem;
  line-height: 3rem;
  height: 48px;
}

.jp {
  color: #555;
  font-size: 0.9rem;
}

@media screen and (max-width: 640px) {
  .link {
    width: 100vw;
  }

  .text {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
}
</style>