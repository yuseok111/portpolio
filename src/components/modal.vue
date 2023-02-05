<template>
	<div class="modal-container" @click="modalToggle">
		<img :src="src" class="modal-box" />
	</div>
</template>
<script>
	import { onMounted, ref } from 'vue';
	import clone1 from '../assets/clone1.png';
	import clone2 from '../assets/clone2.png';

	export default {
		name: 'modal',

		props: {
			imgMode: String,
			modalToggle: Function,
		},

		setup(props) {
			const src = ref('');
			const changeDiv = () => {
				const div = document.getElementsByClassName('modal-container')[0];
				div.style.width = window.innerWidth + 'px';
				div.style.height = window.innerHeight + 'px';
			};

			onMounted(() => {
				changeDiv();
				switch (props.imgMode) {
					case 'movie':
						src.value = clone1;
						break;

					case 'market':
						src.value = clone2;
						break;

					case 'museum':
						src.value = clone1;
						break;

					case 'clone1':
						src.value = clone1;
						break;

					case 'clone2':
						src.value = clone1;
						break;

					case 'clone3':
						src.value = clone1;
						break;

					default:
						src.value = '';
						break;
				}
			});

			return {
				src,
			};
		},
	};
</script>

<style scoped lang="scss">
	.modal-container {
		position: fixed;
		top: 0;
		background-color: rgba(0, 0, 0, 0.7);
		z-index: 3;
		cursor: pointer;
		.modal-box {
			width: 300px;
			height: 300px;
			position: fixed;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			cursor: default;
		}
	}
</style>
