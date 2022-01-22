<script>
import { Line } from 'vue-chartjs'

export default {
  extends: Line,
  props: {
    increase: {
      type: Boolean,
      required: true,
    },
    datasets: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      gradient: null,
      gradient2: null,
    }
  },
  mounted() {
    this.gradient = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)
    this.gradient.addColorStop(0.1119, 'rgba(95, 223, 146, 0.5)')
    this.gradient.addColorStop(0.1118, 'rgba(95, 223, 146, 0.3)')
    this.gradient.addColorStop(0.93, 'rgba(196, 196, 196, 0)')

    this.gradient2 = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)
    this.gradient2.addColorStop(0, 'rgba(255, 189, 189, 0.5)')
    this.gradient2.addColorStop(0.94, 'rgba(196, 196, 196, 0)')

    this.renderChart(
      {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
        datasets: [
          {
            label: 'Data One',
            borderColor: this.increase ? '#28C165' : '#F4574D',
            borderWidth: 1,
            backgroundColor: this.increase ? this.gradient : this.gradient2,
            data: this.datasets,
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
