<template>
	<section id="Intro" class="main">
		<swiper
			:direction="'vertical'"
			:centeredSlides="true"
			:autoplay="{
				delay: 2500,
				disableOnInteraction: false,
				loop: true,
				loopAdditionalSlides: 1,
			}"
			:modules="modules"
			class="mySwiper"
		>
			<swiper-slide>성장 하고 싶은</swiper-slide>
			<swiper-slide>소통 할수 있는</swiper-slide>
			<swiper-slide>꾸준 하고 싶은</swiper-slide>
		</swiper>
		<div class="text-box">
			<h1 class="h1">개발자 <span>김유석</span>입니다 :)</h1>
			<p class="sp">2023 PORTFOLIO</p>
		</div>
	</section>
</template>

<script>
	import { Swiper, SwiperSlide } from 'swiper/vue';
	import 'swiper/css';
	import 'swiper/css/pagination';
	import { Autoplay, Pagination } from 'swiper';
	export default {
		components: {
			Swiper,
			SwiperSlide,
		},
		setup() {
			return {
				modules: [Autoplay, Pagination],
			};
		},
	};
</script>
<style scoped>
	/* //////////////////////// */
	.main {
		background-color: black;
		height: 1000px;
		position: relative;
		top: -60px;
	}
	.h1 {
		color: #fff;
		font-size: 80px;
	}
	.h1 span {
		font-weight: bold;
	}
	.text-box {
		position: absolute;
		top: 30%;
		left: 14.5%;
	}
	.sp {
		color: #fff;
		float: left;
	}

	.swiper {
		position: absolute;
		width: 50%;
		height: 10%;
		top: 20%;
		left: 2%;
	}

	.swiper-slide {
		text-align: center;
		font-size: 70px;
		color: #fff;
		/* Center slide text vertically */
		display: flex;
		justify-content: center;
		align-items: center;
	}
	@media screen and (max-width: 1440px) {
		.swiper {
			position: absolute;
			width: 50%;
			height: 10%;
			top: 20%;
			left: 6%;
		}
	}
	@media screen and (max-width: 1024px) {
		.swiper {
			position: absolute;
			width: 50%;
			height: 10%;
			top: 20%;
			left: 8%;
		}
		.h1 {
			color: #fff;
			font-size: 60px;
		}
		.swiper-slide {
			text-align: center;
			font-size: 50px;
			color: #fff;
			/* Center slide text vertically */
			display: flex;
			justify-content: center;
			align-items: center;
		}
	}
</style>
