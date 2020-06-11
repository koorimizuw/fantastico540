<template>
  <div class="menu">
    <nuxt-link class="top" v-if="!istop" to="/">
      <div class="logo">
        <img src="../../assets/img/top_title_icon.png" alt />
        <div class="title">
          <div class="title-main">FANTASTICO540</div>
          <div class="title-sub">Italian Kitchen</div>
        </div>
      </div>
    </nuxt-link>
    <Link
      v-for="(link, i) in links"
      :istop="istop"
      :key="i"
      :to="link.to"
      :en="link.en"
      :jp="link.jp"
    />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Link from "./link.vue";

export default Vue.extend({
  props: ["istop"],
  data() {
    return {
      links: [
        { to: "about", en: "ABOUT US", jp: "お店の紹介" },
        { to: "menu", en: "MENU", jp: "メニュー" },
        { to: "access", en: "ACCESS", jp: "店舗情報" },
        { to: "contact", en: "CONTACT", jp: "お問い合わせ" },
        { to: "faq", en: "?", jp: "FAQ" }
      ]
    };
  },
  components: {
    Link
  }
});
</script>

<style lang="scss" scoped>
.menu {
  height: 80px;
  display: flex;
  justify-content: center;
  background-color: #eee;
  align-items: center;
}

.top {
  text-decoration: none;
}

.logo {
  background-color: #888888;
  height: 64px;
  width: 260px;
  display: flex;
  align-items: center;
  color: #fff;
  img {
    height: 40px;
    margin: 0 10px;
  }
}

.title {
  font-weight: 100;
  &-main {
    font-size: 1.3rem;
  }
  &-sub {
    font-size: 1rem;
  }
}

.link + .link::before {
  content: "";
  display: block;
  width: 1px;
  height: 50px;
  background-color: #555;
  margin: 15px 0;
}

@media screen and (max-width: 640px) {
  .menu {
    flex-direction: column;
    height: auto;
  }

  .link + .link::before {
    display: none;
  }
}
</style>