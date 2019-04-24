<template>
	<div>
		<h1 class="title"> {{ title }} </h1>
		<grid v-bind:header="header"></grid>
	</div>
</template>

<script>
	import Grid from './components/Grid.vue';

	export default {
		data () {
			return {
				title: 'La Tentatrice',
				header: ['Qty', 'Sugar', 'Fat', 'MSNF', 'Other solids', 'Total solids', 'Water', 'Unit cost', 'Total cost']
			}
		},
		components: {
			Grid
		}
	}; 
</script>

<style scoped>
	.title { color: red };
</style>
