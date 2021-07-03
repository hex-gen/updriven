<template>
    <div v-for="i in dataset" class="actinfo-container bshadow ovf-hidden">
        <div class="top-container">
            <h6 class="xxs fw-500 color-01">
                Activity infomation
                <a class="icon mr-2" href="" style="float: right;">
                    <img src="/assets/img/icon/share.png" alt="share" />
                </a>
            </h6>
        </div>
        <div class="content-container bg-fgray">
            <p class="xxs fw-500 mt-3 ml-3">View Time
                <a class="icon mr-2" href="" style="float: right;">
                    <img src="/assets/img/icon/clock.png" alt="clock" />
                </a>
            </p>
            <h5 class="mt-6 text-center fw-500">{{i.viewtime}}hr</h5>
            <p class="xxs text-center color-gray">Total content watched</p>
            <div class="chart-container " style= "height:55%; width:100%;">
                <monthly-chart class="pt-2" style="width: 100%; height: 100%"/>
            </div>
        </div>
        <div class="content-container bg-fgray">
            <p class="xxs fw-500 mt-3 ml-3">Attendance Average</p>
            <div style= "height:90%; width:100%;">
                <doughnut-chart style="width: 100%; height: 100%"/>
            </div>
        </div>
        <div class="content-container bg-fgray">
            <p class="xxs fw-500 mt-3 ml-3">Most viewed careers</p>
            <p class="text-2xl text-center fw-500" style="margin-top:3rem">{{i.mostviewcareers1}}</p>
            <p class="text-xs text-center fw-500 color-gray" style="margin-top:2rem">{{i.mostviewcareers2}}</p>
            <p class="text-xs text-center fw-500 color-gray" >{{i.mostviewcareers3}}</p>
            <p class="text-xs text-center fw-500 color-gray" >{{i.mostviewcareers4}}</p>
        </div>
    </div> 
</template>

<script>
import DoughnutChart from './Doughnut-chart.vue'
import MonthlyChart from './MonthlyChart.vue'

export default {
    name: 'ActivityInfo',
    components: {
        MonthlyChart,
        DoughnutChart
    },
    data() {
        return {
        dataset: [
            {
                viewtime: '75',
                mostviewcareers1 :'#Programmer',
                mostviewcareers2 :'#Engineer',
                mostviewcareers3 :'#Scientist',
                mostviewcareers4 :'#IT manager'
            }
        ]
    }
  }
}
</script>