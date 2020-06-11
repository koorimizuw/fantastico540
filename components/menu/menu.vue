<template>
  <div class="menu">
    <Title en="Menu" jp="メニュー" />
    <Section v-for="section in menu" :key="section.id" :section="section" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Title from "../title.vue";
import Section from "./section.vue";

export default Vue.extend({
  data() {
    return {
      menu: [
        {
          id: 1,
          title: "Pizza	［ピッツァ］",
          items: [
            {
              name: "モッツアレラチーズとバジリコのピッツァ",
              price: "￥1,100"
            },
            {
              name: "アンチョビとオリーブのピッツァ",
              price: "￥1,180"
            },
            {
              name: "ベーコンとソーセージのピッツァ",
              price: "￥1,290"
            },
            {
              name: "魚介のピッツァ",
              price: "￥1,320"
            },
            {
              name: "フレッシュトマトを散らしたマルゲリータピッツァ",
              price: "￥1,320"
            }
          ]
        },
        {
          id: 2,
          title: "Pasta	［パスタ］",
          items: [
            {
              name: "トマトとニンニクのスパゲティ",
              price: "￥950"
            },
            {
              name: "漁師風スパゲティ ペスカトーレ",
              price: "￥990"
            },
            {
              name: "蒸し鶏とほうれん草、松の実のペペロンチーノスパゲティ",
              price: "￥980"
            },
            {
              name: "渡り蟹のトマトクリームスパゲティカルボナーラ",
              price: "￥1,010"
            },
            {
              name: "スモークサーモンのクリームソーススパゲティ",
              price: "￥990"
            }
          ]
        },
        {
          id: 3,
          title: "Insalata	［サラダ］",
          items: [
            {
              name: "いろいろ野菜の菜園風サラダ",
              price: "￥1,100"
            },
            {
              name: "カプリチョーザのシーザーサラダ",
              price: "￥1,180"
            },
            {
              name: "イカとツナのサラダ",
              price: "￥1,290"
            },
            {
              name: "イタリア産 生ハムのサラダ",
              price: "￥1,320"
            },
            {
              name: "ヤリイカのリング揚げ サラダ仕立て",
              price: "￥1,320"
            }
          ]
        }
      ]
    };
  },
  components: {
    Title,
    Section
  }
});
</script>

<style lang="scss" scoped>
.menu {
  margin-bottom: 100px;
}
</style>