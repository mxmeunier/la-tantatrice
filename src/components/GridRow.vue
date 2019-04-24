<template>
	<div class="grid-row">
		<grid-cell :v-for="size"></grid-cell>
	</div>
</template>

<script>
	import GridCell from './GridCell.vue'

	export default {
		props: {
			size: {
				type: Number,
				required: true
			}
		},
		components: {
			GridCell
		}
	}
</script>

<style scoped>
	.grid-row { display: table-row }
</style>
