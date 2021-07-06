<template>
    <div class="recentevent-container bshadow" >
        <h6 class="xxs fw-500 color-01">
            Recent events joined
        </h6>
        <div class="contain2-container pl-1">
            <div v-for="i in dataset">
                <eventcontent :link="i.link" :image="i.image" :btnText="i.btnText" :head="i.head" :date="i.date" :hashtag="i.hashtag" :numberpeople="i.numberpeople" style="float:left;"/>
            </div>
        </div>
    </div>
</template>

<script>
import eventcontent from './eventcontent.vue'

export default {
    name: 'RecentEvent',
    components: { eventcontent 
    },
    data() { 
        return {
            dataset: [{
            link: '#',
            image: `/assets/img/content/01.jpg`,
            btnText: 'JOINED',
            head: 'Master Industry 4.0 Design with Zelynth and Python',
            date: '10:10 AM - 5:00 PM / MAY 28th',
            hashtag: '#Programmer',
            numberpeople: '241'
        },
        {
            link: '#',
            image: `/assets/img/content/02.jpg`,
            btnText: 'PASSED',
            head: 'Computer Programmer Job Description',
            date: '10:00 AM - 5:00 PM / Aprill 1st',
            hashtag: '#Programmer',
            numberpeople: '577'
        },
        {
            link: '#',
            image: `/assets/img/content/02.jpg`,
            btnText: 'PASSED',
            head: 'Computer Programmer Job Description',
            date: '10:00 AM - 5:00 PM / Aprill 1st',
            hashtag: '#Programmer',
            numberpeople: '577'
        },
        {
            link: '#',
            image: `/assets/img/content/02.jpg`,
            btnText: 'PASSED',
            head: 'Computer Programmer Job Description',
            date: '10:00 AM - 5:00 PM / Aprill 1st',
            hashtag: '#Programmer',
            numberpeople: '577'
        }]
        }
    }
}
</script>