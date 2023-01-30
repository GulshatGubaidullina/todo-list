<template>
	<div class="modal" v-if="show" @click.stop="hideDialog">
		<div @click.stop class="modal__content">
			<slot></slot>
		</div>
	</div>
</template>

<script>
import toggleMixin from '@/mixins/toggleMixin';

export default {
	name: 'MyModal',
	mixins: [toggleMixin]
}
</script>

<style scoped>
.modal {
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	position: fixed;
	display: flex;
	background: rgba(0, 0, 0, 0.5);
}

.modal__content {
	margin: auto;
	padding: 20px;
	background: white;
	border-radius: 15px;
	font-size: 20px;
}
</style>