<template>
  <div class="contact">
    <Header :istop="false" />
    <Title en="CONTACT" jp="お問い合わせ" />
    <div class="form">
      <div class="info">
        予約に関することや、当店に対するご意見ご感想、
        <br />お問い合わせなど、こちらのフォームから気軽にお尋ねください
      </div>
      <form class="main">
        <div class="item" v-for="item in form" :key="item.id">
          <label class="title" :for="item.id">{{item.title}}：</label>
          <input
            v-if="item.style == 0"
            class="input"
            type="text"
            :placeholder="item.placeholder"
            :id="item.id"
          />
          <textarea v-if="item.style == 1" class="input textarea" :id="item.id"></textarea>
        </div>
      </form>
      <div class="info">
        お送りいただいた、お名前やメールアドレスは、
        <br />こちらの連絡用以外には使用いたしません。
      </div>
      <div class="send">
        <button class="btn">送信</button>
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
      form: [
        {
          id: "name",
          title: "お名前",
          placeholder: "例）山田　太郎",
          style: 0
        },
        {
          id: "mail",
          title: "メールアドレス",
          placeholder: "例）yamada@sample.com",
          style: 0
        },
        {
          id: "title",
          title: "お問い合わせ表題",
          placeholder: "",
          style: 0
        },
        {
          id: "content",
          title: "お問い合わせ内容",
          placeholder: "",
          style: 1
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
.contact {
  margin-bottom: 100px;
}

.form {
  padding: 50px 0;
  width: 890px;
  height: 770px;
  margin: 30px auto;
  border: 1px solid #ccc;
  color: #666;
}

.info {
  text-align: center;
  margin: 30px auto;
  font-size: 1.1rem;
  line-height: 25px;
}

.main {
  width: 640px;
  margin: 50px auto;
}

.item {
  display: flex;
  justify-content: flex-end;
  margin: 30px 0;
  font-size: 1.3rem;
}

.title {
  margin: 10px;
}

.input {
  width: 60%;
  height: 20px;
  border-radius: 0px;
  border: none;
  background-color: #eee;
  font-size: 1.2rem;
  padding: 10px;
}

.textarea {
  height: 120px;
}

.send {
  text-align: center;
}

.btn {
  width: 100px;
  border-radius: none;
  background-color: #999;
  padding: 10px;
  border: none;
  font-size: 1.1rem;
  color: #fff;
  font-weight: 100;
  &:hover {
    opacity: 0.8;
    transition: 0.5s;
    cursor: pointer;
  }
}

@media screen and (max-width: 640px) {
  .form {
    width: 90vw;
    height: auto;
  }

  .info {
    margin: 30px 20px;
  }

  .main {
    width: 80vw;
  }

  .item {
    flex-direction: column;
    width: 100%;
  }

  .input {
    width: 95%;
  }
}
</style>