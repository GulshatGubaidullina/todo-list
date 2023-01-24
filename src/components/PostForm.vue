<template>
	<form class="my-form" @submit.prevent>
		<h4>Создание поста</h4>
		<MyInput v-model="post.title" placeholder="Название"></MyInput>
		<MyInput v-model="post.body" placeholder="Описание"></MyInput>
		<MyButton class="form__btn" @click="createPost">Создать</MyButton>
	</form>
</template>

<script>

export default {
	data() {
		return {
			post: {
				title: '',
				body: '',
			}
		}
	},
	methods: {
		createPost() {
			this.post.id = Date.now();
			this.$emit('create', this.post);
			this.post = {
				title: '',
				body: '',
			}
		}
	}
}
</script>

<style scoped>
.my-form {
	display: flex;
	flex-direction: column;
}

.form__btn {
	align-self: flex-end;
	margin-bottom: 10px;
}
</style>