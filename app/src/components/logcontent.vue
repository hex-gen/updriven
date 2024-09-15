<template>
    <div class="mt-2 ovf-hidden" style="width: 100%; height:4rem">
        <img style="width: 13%; height:100%; max-width:13%; max-height:100%; object-fit:cover; float:left;" :src="image" alt="profile" />
        <Button @click="() => TogglePopup('buttonTrigger')"
            :href="link" classer="d-block" style="margin-top:2em; background:url(/assets/img/icon/dots.png) no-repeat; cursor:pointer; float:right"
        />
        <popup v-if="popupTriggers.buttonTrigger" :TogglePopup="() => TogglePopup('buttonTrigger')">
		    </popup>
        <p class="text-xs fw-500" style="margin-left:6rem;"> {{head}}</p>
        <p class="text-2xs fw-500 color-gray" style="margin-left:6rem;">{{comment}}</p>
        <p class="text-2xs fw-500 color-gray" style="margin-left:6rem;">{{group_post}} {{time}}</p>
    </div>
</template>

<script>
import { ref } from 'vue';
import Popup from './Popup.vue';
export default {
  components: { Popup },
  name: 'logcontent',
  props: {
    link: { type: String, default: '' },
    image: { type: String, default: '' },
    head: { type: String, default: '' },
    comment: { type: String, default: '' },
    group_post: { type: String, default: '' },
    time: { type: String, default: '' }
  },
  setup () {
		const popupTriggers = ref({
			buttonTrigger: false
		});
		const TogglePopup = (trigger) => {
			popupTriggers.value[trigger] = !popupTriggers.value[trigger]
		}
		return {
			Popup,
			popupTriggers,
			TogglePopup
		}
	}
}
</script>