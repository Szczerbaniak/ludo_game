<!-- @format -->
<template lang="html">
	<div class="base-container">
		<SlotComponent
			v-for="slot in 4"
			:key="slot"
			:color="player.color"
		></SlotComponent>
	</div>
</template>
<script>
import SlotComponent from "./SlotComponent.vue";
export default {
	components: {
		SlotComponent,
	},
	props: {
		player: Object,
	},
};
</script>
<style lang="css">
.base-container {
	display: grid;
	grid-template-columns: 1fr 1fr;
	grid-template-rows: 1fr 1fr;
	height: fit-content;
	width: fit-content;
}
</style>
