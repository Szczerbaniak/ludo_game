<!-- @format -->

<template>
	<BaseComponent
		v-for="player in players"
		:player="player"
		v-bind:key="player.id"
		:class="'row ' + player.color"
	></BaseComponent>
	<HomeComponent
		v-for="player in players"
		:key="player.id"
		:player="player"
	></HomeComponent>
	<FieldComponent
		v-for="field in 40"
		:key="field"
		:fieldId="field"
	></FieldComponent>
</template>

<script>
import BaseComponent from "./BaseComponent.vue";
import FieldComponent from "./FieldComponent.vue";
import HomeComponent from "./HomeComponent.vue";

export default {
	components: {
		HomeComponent: HomeComponent,
		BaseComponent,
		FieldComponent,
	},
	props: {
		player: Object,
	},

	data: function () {
		return {
			players: [
				{
					id: "1",
					color: "red",
				},
				{
					id: "2",
					color: "green",
				},
				{
					id: "3",
					color: "blue",
				},
				{
					id: "4",
					color: "yellow",
				},
			],
		};
	},
};
</script>
