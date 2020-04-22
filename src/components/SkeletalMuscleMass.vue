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
            label: "骨骼肌重（kg）",
            data: this.bodyDatas.map(data => data.skeletal_muscle_mass),
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
          text: "骨骼肌重"
        }
      }
    );
  }
};
</script>