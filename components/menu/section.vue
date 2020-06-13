<template>
  <div class="section" :class="{reverse: section.id % 2 == 0}">
    <img class="img" :src="require(`../../assets/img/menu_food_0${section.id}.png`)" alt />
    <div class="detail">
      <SubTitle :text="section.title" />
      <div class="item" v-for="(item, i ) in section.items" :key="i">
        <div class="name">{{item.name}}</div>
        <div class="price">{{item.price}}</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import SubTitle from "../subtitle.vue";
export default Vue.extend({
  props: ["section"],
  components: {
    SubTitle
  }
});
</script>

<style lang="scss" scoped>
.section {
  width: 960px;
  margin: 0 auto 60px;
  display: flex;
  color: #666;
}

.reverse {
  flex-direction: row-reverse;
}

.detail {
  margin: 0 20px;
  flex: 1;
}

.item {
  display: flex;
  justify-content: space-between;
  margin: 20px 0;
  font-size: 1.2rem;
}

@media screen and (max-width: 640px) {
  .section {
    flex-direction: column;
    width: 80vw;
    margin: 30px auto;
    img {
      margin: 30px 0;
    }
  }
}
</style>