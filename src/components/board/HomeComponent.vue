<!-- @format -->

<template>
	<SlotComponent
		class="home-container"
		v-for="slot in 4"
		:key="slot"
		:color="player.color"
	></SlotComponent>
</template>
<script>
import SlotComponent from "./SlotComponent.vue";

export default {
	components: { SlotComponent },
	props: {
		player: Object,
	},
};
</script>
<style lang="css"></style>
