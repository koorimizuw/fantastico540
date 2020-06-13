<template>
  <div>
    <div class="visual">
      <div class="main">
        <img src="../assets/img/top_title_icon.png" alt />
        <div class="title">
          <div class="title-main">FANTASTICO540</div>
          <div class="title-sub">Italian Kitchen</div>
        </div>
      </div>
    </div>
    <Header :istop="true" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Header from "~/components/header/header.vue";

export default Vue.extend({
  components: {
    Header
  }
});
</script>

<style lang="scss" scoped>
.visual {
  background-image: url("../assets/img/top_main_visual.png");
  background-size: cover;
  background-position: center;
  width: 100vw;
  min-width: 800px;
  height: calc(100vh - 160px);
}

.main {
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba(0, 0, 0, 0.5);
  //width: 100vw;
  padding: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title {
  color: #fff;
  font-weight: 100;
  margin: 0 20px;
  &-main {
    font-size: 3rem;
  }
  &-sub {
    font-size: 2rem;
  }
}

@media screen and (max-width: 640px) {
  .visual {
    min-width: auto;
  }

  .main {
    width: auto;
    display: block;
    text-align: center;
  }

  .title {
    margin: auto;
  }
}
</style>
