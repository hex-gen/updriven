<script>
import { defineComponent } from 'vue'
import { Line } from 'vue3-chart-v2'

export default defineComponent({
    name: 'MonthlyChart',
    extends: Line,
    mounted () {
        // Overwriting base render method with actual data.
        this.renderChart(
        {
            labels: ['Mar', 'Apr', 'May'],
            datasets: [
                {
                    backgroundColor: '#166c74', 
                    data: [3, 4, 2],
                    tension: 0.1,
                }
            ]
        },{
            
            responsive: true,
            maintainAspectRatio: false,
            legend: {
                display: false
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
                    
                }]
            }
        })
    }
})
</script>