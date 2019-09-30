<template>
	<div id="header">
		<h2 class="h2">this is a header components</h2>
		<br>
		{{title}}
		<button @click="btn1()">button</button>
	</div>
</template>

<script>
	import myalert from "../model/myalert.js";
	export default {
		data() {

		},
		methods: {
			btn1() {
				myalert("hello");
			}
		},
		props:['title']
	}
</script>

<style>
	h2 {
		color: red
	}
</style>