<!-- @format -->
<template>
	<div :class="' slot ' + color"></div>
</template>
<script>
export default {
	props: {
		color: String,
		fieldId: Number,
	},
};
</script>
<style lang="css" scoped>
.slot {
	border: 1px rgb(209, 209, 209) solid;
	border-radius: 5px;
	height: 30px;
	margin: 1px;
	width: 30px;
}
.red {
	background-color: rgb(255, 65, 40);
}
.green {
	background-color: rgb(88, 255, 55);
}
.blue {
	background-color: rgb(54, 54, 255);
}
.yellow {
	background-color: rgb(255, 255, 30);
}
</style>
