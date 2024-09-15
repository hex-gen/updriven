<template>
    <TopNav />
    <div class="app-container">
        <div class="left-container">
            <div class="wrapper" data-simplebar>
            <LeftNav @on-click="(tab) => onClickTab(tab)" />
            </div>
        </div>
        <Banner />
        <div class="middleact-container">
            <ActivityInfo />
        </div>
        <div class="middle22-container">
            <Topmantor />
        </div>
        <div class="middle12-container">
            <Activitylog />
        </div>
        <div class="middleevent-container">
            <RecentEvent />
        </div>
    </div>
</template>

<script>
import TopNav from '../../components/TopNav';
import LeftNav from '../../components/LeftNav';
import Banner from '../../components/Banner';
import ActivityInfo from '../../components/ActivityInfo';
import Activitylog from '../../components/Activitylog.vue';
import Topmantor from '../../components/Topmantor.vue';
import RecentEvent from '../../components/RecentEvent.vue';
export default {
    name: 'UserActivityPage',
    components: {
        TopNav,
        LeftNav,
        Banner,
        ActivityInfo,
        Activitylog,
        Topmantor,
        RecentEvent
    },
    mounted() {
        AOS.init({ easing: 'ease-in-out-cubic', duration: 750, once: true, offset: 10 });
    },
    methods: {
        createPost(post) {
            this.$refs['posts'].createPost(post);
        },
        onClickTab(tab) {
            if(tab.link=='javascript:'){
                this.$refs['posts'].updateCategory(tab);
            }else{
                window.location.href = tab.link;
            }
        }
    }
}
</script>