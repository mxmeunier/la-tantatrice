<template>
	<div id="grid">
		<grid-header :header="header"></grid-header>
		<grid-row :size="rowSize"></grid-row>
	</div>
</template>

<script>
	import GridHeader from './GridHeader.vue'
	import GridRow from './GridRow.vue'

	export default {
		props: {
			header: {
				type: Array,
				required: true
			} 
		},
		components: {
			GridHeader,
			GridRow
		},
		computed: {
			rowSize: function() {
				return this.header.length;
			}
		}
	};
</script>

<style scoped>
	#grid { 
		border: 1px solid black;
		display: table;
		width: 100%;
	};
</style>
