<template>
  <div id="search-ip">
    <h2>ここにIPが表示されます</h2>
    <div>
      <input type="button" value="IPを取得する" @click="getIp" />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    getIp: function () {
      //自身のIPを取得する処理
    },
  },
};
</script>
