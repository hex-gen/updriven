<template>
  <div>
    <a v-if="image" :href="link">
        <img :src="image" alt="Image Content" style="width:7rem"/>
    </a>
    <div v-if="imgText" class="text-container">
      <div> 
          {{imgText}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GroupCard',
  props: {
    link: { type: String, default: '' },
    image: { type: String, default: '' },
    imgText: { type: String, default: '' }
  }
}
</script>
