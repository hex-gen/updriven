<template>
    <div class="bg-white mt-2 mr-2 bshadow" style="width:18rem; height:21rem; ">
        <div style="width:18rem; height:12rem">
            <img style="width:100%; height:100%; max-width:100%; max-height:100%; object-fit:cover;" :src="image" alt="event" />
        </div>
        <div style="width:18rem; height:6rem ">
            <p class="text-s fw-500 ml-3 mt-2">{{head}}</p>
            <p class="text-xs fw-500 ml-3 color-gray">{{date}}</p>
            <p class="text-xs fw-500 ml-3 color-gray">{{hashtag}}</p>
        </div>
        <div style="width:18rem; height:2rem">
            <p class="text-xs fw-500 ml-3 mt-2 color-gray" style="float:left"> {{numberpeople}} people joined</p>
            <Button 
                href="#" classer="d-block btn-color-01 btn-sm pl-5 pr-5 mr-3" 
                :text="btnText" style="float:right"
            />
        </div>
    </div>
</template>

<script>
export default {
  name: 'eventcontent',
  props: {
    link: { type: String, default: '' },
    image: { type: String, default: '' },
    btnText: { type: String, default: '' },
    head: { type: String, default: '' },
    date: { type: String, default: '' },
    hashtag: { type: String, default: '' },
    numberpeople: { type: String, default: '' },
    color: { type: String, default: '' }
  }
}
</script>