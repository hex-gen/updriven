<template>
    <div class="mantor-container mt-3">
        <img style="max-width:25%; max-hight:25%; float:left;" :src="image" alt="profile" />
        <p class="text-nm fw-500" style="margin-left:6rem;"> {{name}}</p>
        <p class="text-3xs fw-500 color-gray" style="margin-left:6rem;"> {{job}}</p>
        <p class="text-xs fw-500" style="margin-left:6rem;"> {{hashtag}}</p> 
    </div>
</template>

<script>
export default {
  name: 'mantor',
  props: {
    image: { type: String, default: '' },
    name: { type: String, default: '' },
    job:  { type: String, default: '' },
    hashtag:  { type: String, default: '' }
  }
}
</script>