<script>
// you can import in a particular component and register the component like below
import VueApexCharts from 'vue3-apexcharts'
export default {
  components: {
    Apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        chart: {
          id: 'vuechart-example',
        },
        xaxis: {
          categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998],
        },
      },
      series: [
        {
          name: 'series-1',
          data: [30, 40, 35, 50, 49, 60, 70, 91],
        },
      ],
    }
  },
}
</script>

<template>
  <div>
    <div>
      <Apexchart
        width="500"
        type="bar"
        :options="chartOptions"
        :series="series"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>
