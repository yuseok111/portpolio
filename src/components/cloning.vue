<template>
	<section id="Webclon">
		<div class="cloneWrap">
			<h1>CLONE</h1>
			<div class="clone_boxs">
				<div class="clone_box">
					<img src="../assets/clone1.png" alt="" />
					<div class="ss">도시락통</div>
					<ul>
						<li>클론 기간: <span class="bold">2022 1월~2023 12.29 월</span></li>
						<li>클론 인원: <span class="bold">1인</span></li>
						<li>배포 링크: <span class="bold">GitHub</span></li>
						<li>설명: 홈페이지 클로닝</li>
					</ul>
					<div class="mokup" @click="modalToggle('clone1')">자세히보기</div>
				</div>
				<div class="clone_box">
					<img src="../assets/clone2.png" alt="" />
					<div class="ss">리치몬드 평창</div>
					<ul>
						<li>클론 기간: <span class="bold">2022 11월 ~ 2023 11.29월</span></li>
						<li>클론 인원: <span class="bold">1인</span></li>
						<li>배포 링크: <span class="bold">GitHub</span></li>
						<li>설명: 홈페이지 클로닝</li>
					</ul>
					<div class="mokup" @click="modalToggle('clone2')">자세히보기</div>
				</div>
				<div class="clone_box">
					<img src="../assets/clone3.png" alt="" />
					<div class="ss">싱그러운 집</div>
					<ul>
						<li>클론 기간: <span class="bold"> 2022 10월 ~ 2023 11월</span></li>
						<li>클론 인원: <span class="bold">1인</span></li>
						<li>배포 링크: <span class="bold">GitHub</span></li>
						<li>설명: 홈페이지 클로닝</li>
					</ul>
					<div class="mokup" @click="modalToggle('clone3')">자세히보기</div>
				</div>
			</div>
		</div>
		<modal :modalToggle="modalToggle" :imgMode="imgMode" v-if="isModal" />
	</section>
</template>

<script>
	import modal from './modal.vue';
	import { reactive, toRefs } from 'vue';

	export default {
		name: 'Cloning',

		setup() {
			const state = reactive({
				imgMode: '',
				isModal: false,
			});

			const modalToggle = str => {
				state.isModal = !state.isModal;
				state.imgMode = str;
			};

			return {
				...toRefs(state),
				modalToggle,
			};
		},

		components: {
			modal,
		},
	};
</script>

<style scoped>
	.cloneWrap {
		padding: 40px 40px;
		height: 1000px;
	}
	h1 {
		text-align: center;
		color: rgb(0, 0, 0);
		padding-top: 40px;
		font-size: 45px;
		position: relative;
	}
	h1::after {
		content: '';
		position: absolute;
		left: 47.95%;
		bottom: -2px;
		height: 2px;
		width: 80px;
		background: rgb(0, 0, 0);
	}
	.clone_box {
		padding-top: 100px;
	}
	.clone_box img {
		width: 500px;
		height: 244.49px;
		border: solid 5px;
		margin-bottom: 90px;
	}
	.clone_boxs {
		display: flex;
		justify-content: space-between;
	}
	.bold {
		font-weight: bold;
	}
	.ss {
		font-weight: bold;
		font-size: 40px;
		position: relative;
		padding-bottom: 20px;
	}
	.ss::after {
		content: '';
		position: absolute;
		left: 0.5%;
		bottom: -2px;
		height: 2px;
		width: 80px;
		background: rgb(0, 0, 0);
	}
	.clone_box ul {
		padding-top: 20px;
	}
	.clone_box ul li {
		padding-top: 10px;
	}
	.mokup {
		border: 1px solid;
		width: 197px;
		left: 35.5%;
		font-size: 16px;
		text-align: center;
		line-height: 45px;
		background: #000000;
		margin-top: 40px;
		color: #fff;
		font-weight: bold;
		cursor: pointer;
	}
</style>
