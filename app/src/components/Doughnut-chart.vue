<script>
import { defineComponent } from 'vue'
import { Doughnut } from 'vue3-chart-v2'

export default defineComponent({
    name: 'DoughnutChart',
    extends: Doughnut,
    mounted () {
        // Overwriting base render method with actual data.
        this.renderChart(
        {
            labels: ['Post', 'Live', 'Group/Event'],
            datasets: [
                {
                    data: [35, 45, 25],
                    backgroundColor: [
                        '#176c74',
                        '#7aa3ab',
                        '#b3c3cb'
                    ],
                }
            ]
        },{
            
            responsive: true,
            maintainAspectRatio: false,
            legend: {
                display: true
            },
            scales: {
                yAxes: [{
                    stacked: true,
                    gridLines: {
                        display: false,
                    },
                    ticks: {
                        display: false //this will remove only the label
                    }
                }],
                xAxes: [{
                    gridLines: {
                        display: false
                    },
                    ticks: {
                        display: false //this will remove only the label
                    }
                }]
            }
        })
    }
})
</script>