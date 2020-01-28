<template>
  <div id="app">
    <div class="container">
      <app-card
        v-for="(company, index) in companies"
        :key="index"
        :company="company"
      ></app-card>
    </div>
  </div>
</template>

<script>
import Card from "./Card";
export default {
  name: "app",
  components: { "app-card": Card },
  data() {
    return {
      companies: [
        {
          name: "LABOT",
          fullName: "株式会社LABOT",
          zipCode: "〒150 - 6090",
          address: "東京都渋谷区恵比寿4-20-4",
          addressExtended: "恵比寿ガーデンプレイスグラススクエアB1",
          employee: {
            position: "Engineer",
            englishName: "Ryosuke Takahashi",
            japaneseName: "高橋涼介",
            email: "takahashi@labot.inc"
          }
        },
        {
          name: "LABOT",
          fullName: "株式会社LABOT",
          zipCode: "〒150 - 6090",
          address: "東京都渋谷区恵比寿4-20-4",
          addressExtended: "恵比寿ガーデンプレイスグラススクエアB1",
          employee: {
            position: "Engineer",
            englishName: "Takumi Fujiwara",
            japaneseName: "藤原拓海",
            email: "fujiwara@labot.inc"
          }
        }
      ]
    };
  }
};
</script>

<style lang="scss">
$bg: #fceeb5;

body {
  background-color: $bg;
  margin: 0 auto;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 15px;
}

.container {
  display: flex;
  align-items: center;
  flex-direction: column;
}
</style>
