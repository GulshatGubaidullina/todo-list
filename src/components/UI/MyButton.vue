<template>
	<button class="my-btn ">
		<slot></slot>
	</button>
</template>

<script>
export default {
	name: 'MyButton'
}
</script>

<style scoped>
.my-btn {
	padding: 10px 15px;
	background: none;
	border: 1px solid rgb(0, 134, 22);
	color: rgb(0, 134, 22);
}
</style>