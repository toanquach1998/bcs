<template>



    <div class="row q-col-gutter-sm" id="chart">
        <apexchart class="col-md-6 col-sm-12 col-xs-12"  type="polarArea" width="380" :options="chartOptions" :series="series"></apexchart>
        <apexchart class="col-md-6 col-sm-12 col-xs-12"  type="polarArea" width="380" :options="chartOptions" :series="series"></apexchart>
      </div>

</template>


<script>

export default {
    name: 'piechart',
    data(){
        return{
 series: [42, 47, 52, 58, 65],
          chartOptions: {
            chart: {
              width: 380,
              type: 'polarArea'
            },
            labels: ['Rose A', 'Rose B', 'Rose C', 'Rose D', 'Rose E'],
            fill: {
              opacity: 1
            },
            stroke: {
              width: 1,
              colors: undefined
            },
            yaxis: {
              show: false
            },
            legend: {
              position: 'bottom'
            },
            plotOptions: {
              polarArea: {
                rings: {
                  strokeWidth: 0
                },
                spokes: {
                  strokeWidth: 0
                },
              }
            },
            theme: {
              monochrome: {
                enabled: true,
                shadeTo: 'light',
                shadeIntensity: 0.6
              }
            }
          },
        }  
    }
}


</script>