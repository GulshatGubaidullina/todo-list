<template>
	<input :value="modelValue" @input="updateInput" class="my-input" type="text">
</template>

<script>
export default {
	name: 'MyInput',
	props: {
		modelValue: [String, Number]
	},
	methods: {
		updateInput(event) {
			this.$emit('update:modelValue', event.target.value)
		}
	}
}
</script>

<style scoped>
.my-input {
	width: 100%;
	border: 1px solid rgb(0, 134, 22);
	padding: 10px 15px;
	margin-bottom: 10px;
}
</style>