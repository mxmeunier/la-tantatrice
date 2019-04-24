<template>
	<div id="grid">
		<grid-header :header="header"></grid-header>
		<grid-row :size="rowSize" v-for="(row, index) in rows" :key="index"></grid-row>
		<button @click="add">Add</button>
	</div>
</template>

<script>
	import GridHeader from './GridHeader.vue'
	import GridRow from './GridRow.vue'

	export default {
		data () {
			return {
				rows: []
			}
		},
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
		},
		methods: {
			add: function() {
				this.rows.push({});
			},
			remove: function(index) {
				this.rows.splice(index, 1);
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