<template>
  <ve-histogram :data="chartData" :settings="chartSettings" />
</template>

<script>
import VeHistogram from 'v-charts/lib/histogram'

export default {
  components: { VeHistogram },

  data() {
    this.chartSettings = {
      metrics: ['用户增长数', '用户流失数'],
      dimension: ['日期']
    }
    return {
      chartData: {
        columns: ['日期', '用户增长数', '用户流失数'],
        rows: [
          { '日期': '2017', '用户增长数': 1393, '用户流失数': 193 },
          { '日期': '2018', '用户增长数': 3530, '用户流失数': 330 },
          { '日期': '2019', '用户增长数': 2923, '用户流失数': 623 },
          { '日期': '2020', '用户增长数': 1723, '用户流失数': 123 }
        ]
      }
    }
  }
}

</script>
