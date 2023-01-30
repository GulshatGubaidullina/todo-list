<template>
	<div class="post">
		<div>
			<div>{{ post.id }}</div>
			<div class="post__title">{{ post.title }}</div>
			<div class="post__description">{{ post.body }}</div>
		</div>
		<div class="post__btns">
			<MyButton @click="$router.push(`/posts/${post.id}`)">Открыть</MyButton>
			<MyButton @click="$emit('remove', post)">Удалить</MyButton>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		post: {
			type: Object,
			required: true,
		}
	}
}
</script>

<style scoped>
.post {
	display: flex;
	align-items: center;
	justify-content: space-between;
	margin-bottom: 15px;
	padding: 15px;
	border: 2px solid rgb(0, 134, 22);
}

.post__btns {
	display: flex;
}
</style>