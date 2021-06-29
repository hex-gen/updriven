<template>
  <h6 class="fw-600">Groups You Manage</h6>
  <div class="Group-show-row">
    <div class="Group-show-column">
    <div v-for="(card, i) in dataset" :key="i" class="grid sm-45" style="margin: 0 0.3rem;">
      <GroupCard :link="card.link" :image="card.image" :imgText="card.imgText" class ="group-text group-image text-position" />
    </div>
    </div>
  </div>
</template>

<script>
import GroupCard from './GroupCard'

export default {
  name: 'ShowGroup',
  components: {
    GroupCard
  },
  data() {
    return {
      user: this.$store.getters.user,
      dataset: []
    }
  },
  mounted() {
    for(let i=0; i<2; i++){
      this.dataset.push({
        link: '#',
        image: `/assets/img/group/group_manage/0${i+1}.jpg`,
        imgText: `0${i+1}.jpg`
      });
    }
  }
}
</script>