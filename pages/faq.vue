<template>
  <div class="faq">
    <Header :istop="false" />
    <Title en="FAQ" jp="よくあるお問い合わせ" />
    <div class="info">
      お客様からレストランへお寄せいただくご質問の中から、
      <br />代表的なものをご紹介しております。
    </div>
    <div class="main">
      <div class="section" v-for="(item, i) in faq" :key="i">
        <div class="q">
          <span>Q</span>
          <span>{{item.q}}</span>
        </div>
        <div class="a">
          <span>A</span>
          <span>
            <p v-for="(text, j) in item.a" :key="j">{{text}}</p>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Header from "~/components/header/header.vue";
import Title from "~/components/title.vue";

export default Vue.extend({
  data() {
    return {
      faq: [
        {
          q: "予約は必要ですか？",
          a: [
            "プラン内容により必ずご予約が必要な場合もございますが、完全予約制ではありません。ただ、お待ちになる事のないよう事前のご予約をお勧めいたします。また、曜日、時間帯によってはご予約をお受けできない場合もございます。詳しくはお問い合わせください。"
          ]
        },
        {
          q: "駐車場はありますか？金額は？",
          a: [
            "申し訳ございません。提携駐車場などはございません。近隣の駐車場では大体30分400円が相場です。駐車場毎に価格が若干異なりますのでご注意ください。"
          ]
        },
        {
          q: "バリアフリーですか？",
          a: [
            "一部段差がございますが、その箇所以外においてはバリアフリーとなっております。移動に支障は無いかと存じます。"
          ]
        },
        {
          q: "貸切はできますか？",
          a: [
            "土日に限りまして貸切を行っております。1週間以上前からのご予約になりますので、ご注意ください。"
          ]
        },
        {
          q: "写真撮影は問題ありませんか？",
          a: [
            "皆様楽しくお食事いただきたく思いますので、写真撮影自体は問題ございません。料理も事前に許諾も必要ありません。",
            "ただ、周りの皆様に迷惑の無い範囲でお願いします。",
            "迷惑と判断した場合はその場でお断りをさせていただきます。",
            "予めご了承ください。"
          ]
        }
      ]
    };
  },
  components: {
    Header,
    Title
  }
});
</script>

<style lang="scss" scoped>
.faq {
  margin-bottom: 100px;
  color: #666;
}

.info {
  text-align: center;
  margin: 20px auto 60px;
  font-size: 1.1rem;
  line-height: 25px;
}

.main {
  width: 640px;
  margin: 0 auto;
}

.section {
  margin: 10px auto;
  &::before {
    content: "";
    width: 100%;
    height: 1px;
    background-color: #ccc;
    display: block;
    margin: 5px 0 10px;
  }
}

.q {
  font-weight: 600;
  font-size: 1.3rem;
  margin: 10px auto;
}

.a {
  display: flex;
  font-size: 1.1rem;
  margin: 20px auto;
  line-height: 25px;
  span + span {
    margin-left: 8px;
  }
}

@media screen and (max-width: 640px) {
  .main {
    width: 80vw;
  }
}
</style>