<template>
    <div class="actinfo-container bshadow ovf-hidden">
        <div class="top-container">
            <h6 class="xxs fw-500 color-01">
                Top Mantor
            </h6>
        </div>
        <div v-for="i in dataset" style="overflow:hidden">
            <mantor :image="i.image" :name="i.name" :job="i.job" :hashtag="i.hashtag"/>
        </div>
    </div>
</template>

<script>
import mantor from './mantor.vue'
export default {
    name: 'Topmantor',
    components: { 
        mantor 
    },
    data() { 
        return {
        dataset: [{
            image: `/assets/img/profile/01.jpg`,
            name: `Lila Nelson`,
            job: 'Software developer',
            hashtag: '#Programmer'
        },
        {
            image: `/assets/img/profile/02.jpg`,
            name: `Avery Cooper`,
            job: 'Computer system engineer',
            hashtag: '#Programmer'
        }]
        }
    }
  
}
</script>