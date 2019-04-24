<template>
	<div> {{ content }} </div>
</template>

<script>
	export default {
		props: {
			content: String
		}
	}
</script>

<style scoped>
	div { 
		border: blue solid 1px;
		display: table-cell;
		text-align: center;
		height: 30px;
	};
</style>


