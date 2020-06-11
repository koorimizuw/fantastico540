<template>
  <div>
    <Header :istop="false" />
    <div class="visual">
      <div class="title">
        <div class="title-main">ABOUT US</div>
        <div class="title-sub">お店の紹介</div>
      </div>
    </div>
    <div class="text">
      <p>オフィス街にあるちいさなイタリア料理店『FANTASTICO540』では、『明るい』と『楽しい』をコンセプトに、味に・食材に・空間を楽しめるように、お料理をご提供しております。</p>
      <p>家族でもお一人でも、利用しやすい家庭的で雰囲気を提供し、楽しく食事やお酒を楽しみたい方が満足できる、幅広いのイタリア料理やワインを取り揃えております。</p>
      <p>
        食材のこだわりは、安心安全であることはもとより、その料理にあった食材を模索し、国内の良質な農家と提携して仕入れを行っております。
        <br />お客様に自信を持ってご提供してまります。
      </p>
      <p>料理に合う自然派のワインを中心に、世界や日本各地のワインを、自信をもって提供いたします。普段のメニューには載らないものも日々仕入れていますので、訪れた時にご確認ください。</p>
    </div>
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
  background-image: url("../assets/img/about_main_visual.png");
  background-size: cover;
  background-position: center;
  width: 100vw;
  //min-width: 800px;
  height: 640px;
}
.title {
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #fff;
  font-weight: 600;
  font-family: "Yu Mincho";
  line-height: 80px;
  text-shadow: #000 0.5em 0.3em 0.6em;
  &-main {
    font-size: 5rem;
  }
  &-sub {
    font-size: 3rem;
  }
}

.text {
  max-width: 640px;
  font-family: "Yu Mincho";
  margin: 60px auto;
  font-size: 1.2rem;
  text-align: center;
  line-height: 30px;
  p + p {
    margin-top: 30px;
  }
}

@media screen and (max-width: 640px) {
  .text {
    margin: 60px 20px;
  }
}
</style>