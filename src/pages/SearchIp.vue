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
  data() {
    return {
      ip: "",
    };
  },
  methods: {
    getIp: function () {
      //自身のIPを取得する処理
      this.ip = "255.255.255.255";
    },
  },
};
</script>
