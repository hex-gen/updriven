<template>
    <div class="actlog-container bshadow ovf-hidden">
        <h6 class="xxs fw-500 color-01">
            Activity Log
        </h6>
        <div class="btn bshadow">
            <Button 
                href="#" classer="color-01 btn-sm pl-5 pr-5" 
                text="Post" style="float:left"
            />
            <Button 
                href="#" classer="color-01 btn-sm pl-5 pr-5" 
                text="Poll" style="float:left"
            />
            <Button 
                href="#" classer="color-01 btn-sm pl-5 pr-5" 
                text="Event" style="float:left"
            />
            <Button 
                href="#" classer="color-01 btn-sm pl-5 pr-5" 
                text="Urgent alert" style="float:left"
            />
            <Button 
                href="#" classer="color-01 btn-sm pl-5 pr-5" 
                text="Live video" style="float:left"
            />
            <Button 
                href="#" classer="d-block btn-color-01 btn-sm pl-5 pr-5" 
                text="DATE" style="float:right"
            />
        </div>
        <div class="contain-container">
            <p class="text-xs fw-500 color-01 mt-2">Yesterday</p>
            <div v-for="i in dataset" >
                <logcontent :link="i.link" :image="i.image" :head="i.head" :comment="i.comment" :group_post="i.group_post" :time="i.time"/>
            </div>
        </div>
    </div> 
</template>

<script>
import logcontent from './logcontent.vue'

export default {
    name: 'Activitylog',
    components: { 
        logcontent
    },
    data() {
    return {
      dataset: [{
            link: '#',
            image: `/assets/img/content/01.jpg`,
            head: 'You searched Groups',
            comment: '"Robot Lover"',
            group_post: 'Only me',
            time: '10:15 PM'
        },
        {
            link: '#',
            image: `/assets/img/content/02.jpg`,
            head: 'You reacted Derrick Sherrills post.',
            comment: '"Lets automate some lights with python?"',
            group_post: 'Public',
            time: '8:07 PM'
        },
        {
            link: '#',
            image: `/assets/img/content/02.jpg`,
            head: 'You reacted Derrick Sherrills post.',
            comment: '"Lets automate some lights with python?"',
            group_post: 'Public',
            time: '8:07 PM'
        },
        {
            link: '#',
            image: `/assets/img/content/02.jpg`,
            head: 'You reacted Derrick Sherrills post.',
            comment: '"Lets automate some lights with python?"',
            group_post: 'Public',
            time: '8:07 PM'
        }]
    }
    }
}
</script>