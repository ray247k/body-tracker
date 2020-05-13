<template>
  <div>經過時間：{{dateDiff}} 天</div>
</template>

<script>
export default {
  props: ["bodyDatas"],
  computed: {
    dateDiff: function() {
      const dateFirst = new Date(this.bodyDatas[0]["date"]);
      const dateLast = new Date(
        this.bodyDatas[[this.bodyDatas.length - 1]]["date"]
      );

      // 預設是微秒，換算成天數
      const dateDiff = (dateLast - dateFirst) / 1000 / 60 / 60 / 24;
      return dateDiff;
    }
  }
};
</script>