<template>
	<select :value="modelValue" @change="changeOption">
		<option disabled value="">Выберите из списка</option>
		<option v-for="option in options" :key="option.value" :value="option.value">
			{{ option.name }}
		</option>
	</select>
</template>

<script>
export default {
	name: 'MySelect',
	props: {
		modelValue: {
			type: String
		},
		options: {
			type: Array,
			default: () => []
		}
	},
	methods: {
		changeOption(event) {
			this.$emit('update:modelValue', event.target.value);
		}
	},
	computed: {
		propModel: {
			get() { return this.prop },
			set(value) { this.$emit('update:prop', value) },
		},
	},
}
</script>

<style scoped>

</style>