<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  props:["bodyDatas"],
  mounted() {
    this.renderChart(
      {
        labels: this.bodyDatas.map(data => data.date),
        datasets: [
          {
            label: "體脂肪率（％）",
            data: this.bodyDatas.map(data => data.percent_body_fat),
            backgroundColor: "transparent",
            borderColor: "rgba(1, 116, 188, 0.50)",
            pointBackgroundColor: "rgba(1, 116, 188, 0.50)"
          }
        ]
      },
      {
        responsive: true,
        maintainAspectRatio: false,
        title: {
          display: true,
          text: `體脂肪率：${(this.bodyDatas[this.bodyDatas.length - 1]['percent_body_fat'] - this.bodyDatas[0]['percent_body_fat']).toFixed(2)} %`
        }
      }
    );
  }
};
</script>