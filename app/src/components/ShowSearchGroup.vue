<template>
  <div class="Group-show-row bshadow" style="height: 12rem; width: 46.5rem;">
    <a v-if="image" :href="link">
        <img :src="image" alt="Image Content" class="img-search-group"/>
    </a>
    <div v-if="imgText">
      <div> 
          {{imgText}}   
      </div>
    </div>
    <div v-if="property">
      <div> 
          {{property}}   
      </div>
    </div>
    <div v-if="members">
      <div> 
          {{members}}   
      </div>
    </div>
    <div v-if="postperday">
      <div> 
          {{postperday}}   
      </div>
    </div> 
    <div v-if="btnText" class="text-container">
      <div class="btns text-center">
        <Button :href="link" classer="btn-color-01" :text="btnText" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ShowSearchGroup',
  props: {
    link: { type: String, default: '' },
    image: { type: String, default: '' },
    imgText: { type: String, default: '' },
    btnText: { type: String, default: '' },
    property: { type: String, default: '' },
    members: { type: String, default: '' },
    postperday: { type: String, default: '' },
  }
}
</script>