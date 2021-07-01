<template>
  <h6 class="fw-600">Groups You Manage</h6>
  <div class="Group-show-row">
    <div class="Group-show-column">

    <div v-for="(card, i) in dataset" :key="i" class="grid" style="margin: 0 0.3rem;">
      <GroupCard :link="card.link" :image="card.image" :imgText="card.imgText" class ="group-text group-image text-position" />
    </div>
    <div style="filter:grayscale(100%);">
      <button type="button" class="btn_add_group">
        <img src="/assets/img/icon/plus-circle.png" class="img-add-group">
        <label style="font-size: 0.5rem;">CREATE A GROUP</label>
      </button>
    </div>
    </div>
  </div>
</template>

<script>
import GroupCard from './GroupCard'

export default {
  name: 'ShowGroup01',
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