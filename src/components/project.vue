<template>
	<section id="Project">
		<div class="ProWrap">
			<h1>PROJECT</h1>
			<div class="project_box">
				<div class="proimg">
					<img src="../assets/pro1.gif" alt="" />
					<div class="mokup" @click="modalToggle('movie')">자세히보기</div>
				</div>
				<div class="title_box">
					<div class="title">쁘띠시네마</div>
					<div class="title-s">
						<span class="bold">반응형,레이아웃등이 난잡하여 리뉴얼을 진행한 프로젝트</span>
					</div>
					<ul>
						<li>프로젝트기간: <span class="bold">2022 10월 ~ 2023 1월</span></li>
						<li>프로젝트 인원 : <span class="bold">1인</span></li>
						<li>프로젝트 배포링크: <span class="bold">GitHub</span></li>
						<li>프로젝트설명</li>
					</ul>
					<div class="info_box">
						<div class="bold">- FRONT-END</div>
						<div>
							메인페이지,로그인/회원가입,예약페이지,영화정보페이지 <br />
							게시판수정삭제업로드,썸네일업로드페이지,반응형웹
						</div>
						<div class="bold">- BACK-END</div>
						<div>
							로그인/회원가입 게시판 (게시,수정,삭제)<br />
							썸네일 업로드 데이터 베이스연결<br />
							전체페이지 노드연결(익스프레스)
						</div>
						<div class="bold">- DEPLOYMENT</div>
						<div>깃허브 연동 CodePipeline,CloudFront등 AWS 서비스를 통한 배포 자동화 구축</div>
						<div class="bold">- USE STACK</div>
						<div>HTML5,CSS,JS,NODE js,Mysql,jQuery</div>
					</div>
				</div>
			</div>
			<div class="project_box">
				<div class="proimg">
					<img src="../assets/pro2.gif" alt="" />
					<div class="mokup" @click="modalToggle('market')">자세히보기</div>
				</div>
				<div class="title_box">
					<div class="title">서문야시장</div>
					<div class="title-s">
						<span class="bold">야시장 레이아웃을 리뉴얼을 진행한 프로젝트</span>
					</div>
					<ul>
						<li>프로젝트기간: <span class="bold">2022 9월 ~ 2023 1월</span></li>
						<li>프로젝트 인원 : <span class="bold">1인</span></li>
						<li>프로젝트 배포링크: <span class="bold">GitHub</span></li>
						<li>프로젝트설명</li>
					</ul>
					<div class="info_box">
						<div class="bold">- FRONT-END</div>
						<div>
							메인페이지,로그인/회원가입,예약페이지,야시장소개페이지 <br />
							게시판 (수정,삭제,업로드),야시장 자세히보기,반응형웹
						</div>
						<div class="bold">- BACK-END</div>
						<div>
							로그인/회원가입 데이터연결 <br />게시판데이터연결 (게시,수정,삭제)<br />
							전체페이지 노드연결(익스프레스)
						</div>
						<div class="bold">- DEPLOYMENT</div>
						<div>깃허브 연동 CodePipeline,CloudFront등 AWS 서비스를 통한 배포 자동화 구축</div>
						<div class="bold">- USE STACK</div>
						<div>HTML5,CSS,JS,NODE js,Mysql,jQuery</div>
					</div>
				</div>
			</div>
			<div class="project_box">
				<div class="proimg">
					<img src="../assets/pro3.gif" alt="" />
					<div class="mokup" @click="modalToggle('museum')">자세히보기</div>
				</div>
				<div class="title_box">
					<div class="title">장욱진 미술관</div>
					<div class="title-s">
						<span class="bold">리뉴얼이 필요한 사이트를골라 리뉴얼을 진행한 팀프로젝트</span>
					</div>
					<ul>
						<li>프로젝트기간: <span class="bold"> 2022 12월 ~ 2023 12.29월</span></li>
						<li>프로젝트 인원 : <span class="bold">3인</span></li>
						<li>프로젝트 배포d링크: <span class="bold">GitHub</span></li>
						<li>프로젝트설명</li>
					</ul>
					<div class="info_box">
						<div class="bold">- FRONT-END</div>
						<div>
							<span class="bold">담당섹션 - </span>메인페이지섹션4,5 ,로그인/회원가입,예약페이지 - <br />

							전시소개 페이지 , 게시판 공지사항 (수정,삭제,업로드),
							<br />오시는길,전시공간소개 , 소장품안내 ,반응형웹
						</div>
						<div class="bold">- BACK-END</div>
						<div>
							로그인/회원가입 게시판 (게시,수정,삭제,유효성검사,데이터연결)<br />
							썸네일 업로드 데이터 베이스연결<br />
							전체페이지 노드연결(익스프레스)
						</div>
						<div class="bold">- DEPLOYMENT</div>
						<div>깃허브 연동 CodePipeline,CloudFront등 AWS 서비스를 통한 배포 자동화 구축</div>
						<div class="bold">- USE STACK</div>
						<div>HTML5,CSS,JS,NODE js,Mysql,jQuery</div>
					</div>
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
		name: 'Project',
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
	div {
		box-sizing: border-box;
	}
	.black-bg {
		width: 100;
		height: 100%;
		background: rgba(0, 0, 0, 0.5);
		position: fixed;
		padding: 20px;
	}
	.white-bg {
		width: 100%;
		background: white;
		border-radius: 8px;
		padding: 20px;
	}
	/* ///모달끝 */
	h1 {
		text-align: center;
		color: #fff;
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
		background: #fff;
	}
	.ProWrap {
		background-color: black;
		height: 100%;
		padding: 0 240px;
		padding-bottom: 150px;
		position: relative;
	}
	.project_box {
		width: 1440px;
		height: 859px;
		background-color: #fff;
		display: flex;
		padding: 50px 0px;
		padding-bottom: 5px;
		margin-top: 110px;
	}
	.proimg {
		position: relative;
		width: 48%;
	}
	.proimg > img {
		position: absolute;
		top: 25%;
		left: 15%;
		width: 500px;
		height: 209px;
		border: 5px solid #000000;
		box-sizing: border-box;
	}
	.mokup {
		position: absolute;
		top: 80%;
		border: 1px solid;
		width: 197px;
		left: 35.5%;
		font-size: 16px;
		text-align: center;
		line-height: 45px;
		background: #000000;
		color: #fff;
		font-weight: bold;
		cursor: pointer;
	}
	.bold {
		font-weight: bold;
	}
	.title_box {
		flex-direction: wrap;
	}

	.title {
		font-family: 'Inter';
		font-weight: 700;
		font-size: 40px;
		line-height: 48px;
		position: relative;
		padding-bottom: 20px;
	}
	.title::after {
		content: '';
		position: absolute;
		left: 0.5%;
		bottom: -2px;
		height: 2px;
		width: 80px;
		background: rgb(0, 0, 0);
	}
	.title-s {
		padding-top: 30px;
		padding-bottom: 15px;
	}
	.title_box ul li {
		padding-top: 15px;
		font-size: 18px;
	}
	_.title_box ul li:last-child {
		padding-bottom: 20px;
	}
	.info_box div {
		padding-bottom: 20px;
	}
	.info_box > div {
		padding-right: 20px;
	}
</style>
