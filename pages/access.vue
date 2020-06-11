<template>
  <div class="access">
    <Header :istop="false" />
    <Title en="ACESS" jp="店舗情報" />
    <div class="map">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12960.619315538932!2d139.77771459356688!3d35.69780736667495!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60188c1d6fb43a83%3A0x4309d3ce448a7a27!2z44OH44K444K_44Or44OP44Oq44Km44OD44OJ5aSn5a2m!5e0!3m2!1sja!2sjp!4v1591835910491!5m2!1sja!2sjp"
        width="100%"
        height="450"
        frameborder="0"
        style="border:0;"
        allowfullscreen
        aria-hidden="false"
        tabindex="0"
      ></iframe>
    </div>
    <div class="section" v-for="(item, i) in info" :key="i">
      <SubTitle :text="item.title" />
      <p class="content" v-for="(content, j) in item.text" :key="j">{{content}}</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Header from "~/components/header/header.vue";
import Title from "~/components/title.vue";
import SubTitle from "~/components/subtitle.vue";

export default Vue.extend({
  data() {
    return {
      info: [
        {
          title: "住所",
          text: ["〒101-0062", "東京都千代田区神田駿河台4-6-B4F"]
        },
        {
          title: "電話番号",
          text: ["03-1234-5678"]
        },
        {
          title: "交通機関",
          text: [
            "・JR「御茶ノ水駅【聖橋口改札】」より徒歩1分",
            "・東京メトロ千代田線「新御茶ノ水駅【B2出口】」直通1分",
            "・東京メトロ丸の内線「御茶ノ水駅【出口1】」より徒歩4分",
            "・JR「秋葉原駅」より徒歩9分",
            "・都営地下鉄新宿線「小川町駅」より徒歩6分"
          ]
        },
        {
          title: "営業時間",
          text: [
            "・定休日 日曜日",
            "・Lunch 11:30-14:00",
            "・Dinner 18:00-23:00"
          ]
        },
        {
          title: "専用駐車場",
          text: ["ありません。近隣の駐車場をご利用ください。"]
        }
      ]
    };
  },
  components: {
    Header,
    Title,
    SubTitle
  }
});
</script>

<style lang="scss" scoped>
.access {
  margin-bottom: 100px;
}

.map {
  width: 890px;
  margin: 0 auto 50px;
}

.section {
  color: #666;
  width: 590px;
  margin: 50px auto;
}

.content {
  font-size: 1.2rem;
  margin: 10px auto;
}

@media screen and (max-width: 640px) {
  .map {
    width: 100vw;
  }

  .section {
    width: 80vw;
  }
}
</style>