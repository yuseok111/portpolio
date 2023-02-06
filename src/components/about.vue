<template>
	<section id="About">
		<div class="main2">
			<h2 class="h2">ABOUT</h2>
		</div>
		<div class="sec1 wrap">
			<div class="pic">
				<img class="img" src="../assets/pic.png" alt="" />
				<div class="info_box">
					<h1 class="info">성장하고 싶은 개발자</h1>
					<h1 class="info2">김유석 입니다</h1>
				</div>
				<ul class="text_box">
					<span>"책임,공유,겸손"</span>
					<li>꾸준히 하는것, 그리고 잘 쉬는 것을 <br />개발 모토로 여기고 성장하고 싶습니다.</li>
				</ul>
			</div>
			<div class="about_main">
				<div class="about_wrap">
					<div class="about_box">
						<div class="title">WHO?</div>
						<ul>
							<li><span class="bolds">김유석</span></li>
							<li>1999.02.24</li>
							<li>010-8731-8942</li>
							<li>dbtjr1441@naver.com</li>
						</ul>
					</div>
					<div class="about_box">
						<div class="title">EDUCATION</div>
						<ul>
							<li>2017 <span class="bold">의정부 공업 고등학교</span></li>
							<li>2019 <span class="bold">서정대학교</span></li>
							<li></li>
						</ul>
					</div>
				</div>
				<div class="about_wrap2">
					<div class="about_box">
						<!-- /섹션 -->
						<div class="title">CERTIFICATE</div>
						<ul>
							<li>2020 <span class="bold">위생사</span></li>
							<li>2019 <span class="bold">식품산업기사</span></li>
							<li>2019 <span class="bold">자동차운전면허 1종</span></li>
							<li>2017 <span class="bold">전자기기 기능사</span></li>
						</ul>
					</div>
					<div class="about_box">
						<div class="title">PROJECTS</div>
						<ul>
							<li>2022 <span class="bold">팀프로젝트-장욱진미술관 리뉴얼</span></li>
							<li>2022 <span class="bold">개인프로젝트-쁘띠시네마 리뉴얼</span></li>
							<li>2022 <span class="bold"> 개인프로젝트-서문야시장 리뉴얼</span></li>
							<li>2022 <span class="bold"> 클론코딩 3종</span></li>
						</ul>
					</div>
				</div>
				<div class="skill_wrap">
					<div class="title">SKILLS</div>
					<div class="ski_flex">
						<div class="skill_01">
							<div>
								<p>- Language</p>
								<img src="../assets/html-5--v2.png" alt="" />
								<img class="css" src="../assets/css3.png" alt="" />
								<img class="java" src="../assets/javascript-logo.png" alt="" />
							</div>
							<div>
								<p>- BACK-END</p>
								<img src="../assets/mysql-logo.png" alt="" />
								&nbsp &nbsp
								<img src="../assets/nodejs.png" alt="" />
							</div>
							<div>
								<p>- BERSION CONTORL</p>
								<img src="../assets/github.png" />
							</div>
						</div>
						<div class="skill_02">
							<div>
								<p>- FRONT-END</p>
								<img
									src="../assets/external-vuejs-an-open-source-javascript-framework-for-building-user-interfaces-and-single-page-applications-logo-bold-tal-revivo.png"
								/>
							</div>
							<div>
								<p>- DESIGN</p>
								<img src="../assets/adobe-photoshop.png" />
								&nbsp
								<img class="ai" src="../assets/adobe-illustrator.png" />
								&nbsp
								<img src="../assets/figma.png" />
							</div>
							<div>
								<p>- DEPLOYMENT</p>
								<img src="../assets/amazon-web-services.png" />
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>
<style scoped>
	.h2 {
		font-size: 45px;
		position: relative;
		font-weight: bold;
		text-align: center;
	}
	.h2::after {
		content: '';
		position: absolute;
		left: 47.95%;
		bottom: -2px;
		height: 2px;
		width: 80px;
		background: #000;
	}
	.img {
		width: 350px;
		height: 350px;
		border-radius: 80px;
		object-fit: cover;
		border: 1px solid #000000;
		filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
		border-radius: 87px;
	}
	.pic {
		width: 42%;
	}
	.wrap {
		padding: 0 175px;
		padding-top: 120px;
		display: flex;
		height: 1200px;
	}
	.info_box {
		padding-top: 20px;
		position: relative;
	}
	.info {
		font-size: 40px;
		font-weight: 500;
	}
	.info2 {
		font-size: 40px;
		font-weight: bold;
	}
	.info_box::after {
		content: '';
		position: absolute;
		left: 0.5%;
		bottom: -8px;
		height: 3px;
		width: 60px;
		background: #000;
	}
	.text_box {
		padding-top: 20px;
	}
	.text_box span {
		font-weight: 700;
		font-size: 26px;
	}
	.text_box li {
		padding-top: 20px;
		font-weight: 700;
		font-size: 20px;
	}
	.title {
		font-weight: 700;
		font-size: 26px;
		padding-bottom: 30px;
	}
	.bold {
		font-weight: bold;
		font-size: 20px;
		padding-left: 20px;
	}
	.bolds {
		font-weight: bold;
		font-size: 20px;
	}

	.about_main {
		display: flex;
		margin-left: 170px;
		height: 500px;
		flex-wrap: wrap;
	}
	.about_wrap {
		margin-right: 170px;
		height: 200px;
	}
	.about_wrap2 {
		padding-bottom: 20px;
	}
	.about_box {
		margin-bottom: 60px;
	}
	.about_box ul li {
		font-weight: 400;
		font-size: 20px;
	}

	.ski_flex {
		display: flex;
	}
	.skill_01 {
		margin-right: 150px;
	}
	.skill_01 img {
		width: 55px;
		height: 55px;
	}
	.skill_02 img {
		width: 55px;
		height: 55px;
	}
	.skill_01 .java {
		width: 45px;
		height: 48px;
	}
	.skill_01 .css {
		width: 53px;
		height: 55px;
	}
	.skill_01 > div > p {
		line-height: 3;
	}
	.skill_02 > div > p {
		line-height: 3;
	}
	.skill_01 p {
		font-size: 18px;
		font-weight: bold;
	}
	.skill_02 p {
		font-size: 18px;
		font-weight: bold;
	}
	.skill_02 .ai {
		width: 55px;
		height: 55px;
	}
	@media screen and (max-width: 1440px) {
		.wrap {
			padding: 28px 7px !important;
			padding-top: 120px;
			display: flex;
			height: 1200px;
		}
	}
	@media screen and (max-width: 1700px) {
		.wrap {
			padding: -3px 175px !important;
			padding-top: 120px;
			display: flex;
			height: 1200px;
		}
	}
	@media screen and (max-width: 1024px) {
		.wrap {
			padding: -3px 175px !important;
			padding-top: 120px;
			display: flex;
			height: 1200px;
			flex-direction: column;
		}
	}
</style>
