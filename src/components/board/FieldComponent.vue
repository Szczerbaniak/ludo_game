<!-- @format -->

<template lang="html">
	<SlotComponent :color="color" :fieldId="fieldId"></SlotComponent>
</template>
<script>
import SlotComponent from "./SlotComponent.vue";

export default {
	components: { SlotComponent },
	props: {
		fieldId: Number,
	},
	computed: {
		color: function () {
			switch (this.fieldId) {
				case 1:
					return "red";
				case 11:
					return "green";
				case 21:
					return "blue";
				case 31:
					return "yellow";
				default:
					return "";
			}
		},
	},
};
</script>
<style lang="css"></style>
