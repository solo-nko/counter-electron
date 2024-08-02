<template>
	<div id="app-container">
		<h1>Counter Electron App</h1>
		<h2>{{ count }}</h2>
		<div class="button" v-on:click="increment(delta)">Increment</div>
		<div class="button" v-on:click="decrement(delta)" >Decrement</div>
	</div>

</template>

<script setup lang="ts">

import { ref } from "vue";

const count = ref(0);
const delta = ref(1);

function increment(increaseBy = 1) {
	count.value += increaseBy;
}

function decrement(increaseBy = 1) {
	count.value -= increaseBy;
}

function setCount(event:Event) {
	const target = event.target as HTMLInputElement;
}


</script>

<style scoped>

#app-container {
	display: flex;
	flex-direction: column;
	align-items: center;
}

.button {
	background-color: aliceblue;
	width: fit-content;
}

</style>