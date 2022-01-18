<script>
import { Line } from 'vue-chartjs'

export default {
  extends: Line,
  data() {
    return {
      gradient: null,
    }
  },
  mounted() {
    this.gradient = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)
    this.gradient.addColorStop(0.1119, '#5FDF92')
    this.gradient.addColorStop(0.1118, 'rgba(95, 223, 146, 0.8)')
    this.gradient.addColorStop(0.93, 'rgba(196, 196, 196, 0)')

    this.renderChart(
      {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
        datasets: [
          {
            label: 'Data One',
            borderColor: '#28C165',
            borderWidth: 1,
            backgroundColor: this.gradient,
            data: [40, 39, 10, 40, 39, 80, 40],
          },
        ],
      },
      {
        responsive: true,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
        elements: {
          point: {
            radius: 0,
          },
        },
        tooltips: {
          callbacks: {
            label: (tooltipItem) => {
              return tooltipItem.yLabel
            },
          },
        },
        scales: {
          yAxes: [
            {
              ticks: {
                display: false,
              },
              gridLines: {
                display: false,
                drawBorder: false,
                color: 'rgba(0, 0, 0, 0)',
              },
            },
          ],
          xAxes: [
            {
              ticks: {
                display: false,
              },
              gridLines: {
                display: false,
                drawBorder: false,
                color: 'rgba(0, 0, 0, 0)',
              },
            },
          ],
        },
      }
    )
  },
}
</script>
