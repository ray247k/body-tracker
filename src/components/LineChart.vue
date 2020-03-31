<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  mounted() {
    this.renderChart(
      {
        labels: [
          "2019/11/19",
          "2019/12/01",
          "2019/12/29",
          "2020/01/30",
          "2020/03/03",
        ],
        datasets: [
          {
            label: "體脂肪率（％）",
            data: [29.4, 28.1, 28.4, 30.3, 29.7],
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
          text: "體脂肪率曲線"
        }
      }
    );
  }
};
</script>