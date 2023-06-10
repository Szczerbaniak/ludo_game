<!-- @format -->

import BaseComponent from './components/board/BaseComponent.vue';

<!-- @format -->

<template>
	<BoardComponent></BoardComponent>
	<!-- {{ displayDraw }} -->
	<!-- <button v-on:click="$refs.dice.draw()">draw</button> -->
	<DiceComponent v-on:draw="draw" ref="dice"></DiceComponent>
</template>

<script>
import DiceComponent from "./components/DiceComponent.vue";

import BoardComponent from "./components/board/BoardComponent.vue";
// import BaseComponent from "./components/board/BaseComponent.vue";
// import FieldComponent from "./components/board/FieldComponent.vue";
// import HomeComponent from "./components/board/HomeComponent.vue";
// import PawnComponent from "./components/board/PawnComponent.vue";
// import SlotComponent from "./components/board/SlotComponent.vue";

export default {
	name: "App",
	components: {
		DiceComponent: DiceComponent,
		BoardComponent: BoardComponent,
		// BaseComponent: BaseComponent,
		// FieldComponent: FieldComponent,
		// HomeComponent: HomeComponent,
		// PawnComponent: PawnComponent,
		// SlotComponent: SlotComponent,
	},
	data: function () {
		return {
			displayDraw: "Nie wylosowano liczby",
		};
	},
	methods: {
		draw: function (value) {
			this.displayDraw = `Wylosowano liczbę ${value}`;
		},
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
