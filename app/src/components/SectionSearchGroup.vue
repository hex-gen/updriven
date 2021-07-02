<template>
  <h6 class="fw-600">You may be interested</h6>
  <div>
    <div>
    <div v-for="(card, i) in dataset" :key="i" >
      <ShowSearchGroup :link="card.link" :image="card.image" :imgText="card.imgText"  :btnText="card.btnText" 
      :property="card.property" :members="card.members" :postperday="card.postperday" />
    </div> 
    </div>
  </div>
</template>

<script>
import ShowSearchGroup from './ShowSearchGroup'

export default {
  name: 'SectionSearchGroup',
  components: {
    ShowSearchGroup
  },
  data() {
    return {
      user: this.$store.getters.user,
      dataset: []
    }
  },
  mounted() {
    for(let i=0; i<6; i++){
      this.dataset.push({
        link: '#',
        image: `/assets/img/group/search_group/0${i+1}.jpg`,
        imgText: `0${i+1}.jpg`,
        btnText: 'JOIN',
        property: 'Public Group',
        members: 'members',
        postperday: 'post a day'
      });
    }
  }
}
</script>