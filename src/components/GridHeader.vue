<template>
	<div class="grid-header">
		<grid-cell
			v-for="title in header"
			v-bind:key="title"
			v-bind:content="title"
		></grid-cell>
	</div>
</template>

<script>
	import GridCell from './GridCell.vue'

	export default {
		props: {
			header: {
				type: Array,
				required: true
			}
		},
		components: {
			GridCell
		}
	}
</script>

<style scoped>
	.grid-header { display: table-row }
</style>
