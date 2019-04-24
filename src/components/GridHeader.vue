<template>
	<div class="grid-header">
		<div class="header-cell"
			v-for="(title, index) in header"
		> {{ title }} </div>
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
		}
	}
</script>

<style scoped>
	.grid-header { display: table-row }
	.header-cell { display: table-cell; border: 1px solid black }
</style>
