<template>
	<div class="navbar">
		<div @click="$router.push('/')">Vue 3</div>
		<div class="navbar__btns">
			<MyButton @click="$router.push('/posts')">К постам</MyButton>
			<MyButton style="margin-left: 20px" @click="$router.push('/about')">К описанию</MyButton>
			<MyButton style="margin-left: 20px" @click="$router.push('/store')">Store</MyButton>
		</div>
	</div>
</template>

<script>

export default {
}
</script>

<style scoped>
.navbar {
	height: 50px;
	display: flex;
	align-items: center;
	padding: 15px;
	background: rgb(196, 216, 199);
	box-shadow: 2px 2px 4px gray;
}

.navbar__btns {
	margin-left: auto;
}
</style>