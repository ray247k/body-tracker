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
            label: "體重（kg）",
            data: this.bodyDatas.map(data => data.body_weight),
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
          text: `體重變化：${(this.bodyDatas[this.bodyDatas.length - 1]['body_weight'] - this.bodyDatas[0]['body_weight']).toFixed(2)} kg`
        }
      }
    );
  }
};
</script>