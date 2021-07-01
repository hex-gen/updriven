<template>
<div style="padding-top: 1rem">
  <div class="Group-show-row bshadow" style="height: 12rem; width: 46.5rem;">
    <div>
    <a v-if="image" :href="link">
        <img :src="image" alt="Image Content" class="img-search-group"/>
    </a>
    </div>
    <div>
      <div v-if="imgText" class="img-text-group">
        <div> 
            {{imgText}}   
        </div>
      </div>
      <div class="property-text-group">
        <div v-if="property">
              {{property}}   
        </div>
        <div v-if="members" class="members-text-group">
              𐤟 {{members}}   
        </div>
      </div>
      <div style="display: flex; padding-top: 4rem;">
      <div v-if="btnText" class="text-container">
        <div class="btns text-center">
          <Button :href="link" classer="btn-color-01" :text="btnText" />
        </div>
      </div>
      <div v-if="postperday" class="postperday-text-group">
        <div> 
            {{postperday}}   
        </div>
      </div> 
      </div>
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