<template>
  <div class="app-container">
    <!-- <ve-line :extend="chartExtend" :data="chartData" :settings="chartSettings"/> -->
    <ve-bar :data="chartData" />
  </div>
</template>

<script>
// import { statOrder } from '@/api/stat'
import VeBar from 'v-charts/lib/bar'
export default {
  components: { VeBar },
  data() {
    return {
      chartData: {
        columns: ['日期', '订单量', '下单用户', '下单率'],
        rows: [
          { '日期': '1/1', '订单量': 1393, '下单用户': 1093, '下单率': 0.32 },
          { '日期': '1/2', '订单量': 3530, '下单用户': 3230, '下单率': 0.26 },
          { '日期': '1/3', '订单量': 2923, '下单用户': 2623, '下单率': 0.76 },
          { '日期': '1/4', '订单量': 1723, '下单用户': 1423, '下单率': 0.49 },
          { '日期': '1/5', '订单量': 3792, '下单用户': 3492, '下单率': 0.323 },
          { '日期': '1/6', '订单量': 4593, '下单用户': 4293, '下单率': 0.78 }
        ]
      },
      chartSettings: {},
      chartExtend: {}
    }
  }
  // created() {
  //   statOrder().then(response => {
  //     // this.chartData = response.data.data
  //     this.chartSettings = {
  //       labelMap: {
  //         'orders': '订单量',
  //         'customers': '下单用户',
  //         'amount': '订单总额',
  //         'pcr': '客单价'
  //       }
  //     }
  //     this.chartExtend = {
  //       xAxis: { boundaryGap: true }
  //     }
  //   })
  // }

}
</script>
