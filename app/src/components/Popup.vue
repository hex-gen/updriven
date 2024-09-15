<template>
	<div class="popup">
		<Button 
			href="#" class="popup-close" @click="TogglePopup()" classer="d-block btn-color-05 btn-sm pl-2 pr-2 mr-1" 
			text="Remove reation " style="float: right;"
        />
		<Button 
			href="#" class="popup-close" @click="TogglePopup()" classer="d-block btn-color-05 btn-sm pl-2 pr-2 mr-1" 
			text="Delete" style="float: right;"
        />
	</div>
</template>

<script>
export default {
	props: ['TogglePopup']
}
</script>
