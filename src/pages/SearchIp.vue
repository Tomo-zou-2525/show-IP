<template>
  <div id="search-ip">
    <!-- data()で定義されたIPをv-textで撮ってくる -->
    <h2 v-text="ip">ここにIPが表示されます</h2>
    <div>
      <input type="button" value="IPを取得する" @click="getIp" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchIp",
  data() {
    return {
      ip: ""
    };
  },
  methods: {
    getIp: function() {
      //自身のIPを取得する処理 axios導入前
      // this.ip = "255.255.255.255";
      //axios導入後
      this.ip = "ipを取得しています";
      //これは、HTTPリクエストを返してくれるWebApi
      //fetchの代わりにaxiosを使うのか
      this.$axios
        .get("https://httpbin.org/get")
        //成功時、
        .then(response => {
          this.ip = response.data.origin;
        })
        .catch(reason => {
          this.ip = "IPの取得に失敗しました";
        });
    }
  }
};
</script>
