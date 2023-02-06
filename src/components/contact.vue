<template>
	<section id="Contact">
		<div class="conwrap">
			<h1>CONTACT</h1>
			<div class="contact_box">
				<div class="left_contact">
					<div>
						<span class="bold">GIT</span>
						<a href="https://github.com/yuseok111" class="s1">github.com</a>
					</div>
					<div>
						<span class="bold">E-MAIL</span>
						<a href="" class="s2">dbtjr1441@naver.com</a>
					</div>
					<div>
						<span class="bold">기술블로그</span>
						<a href="https://velog.io/@dbtjr3569">velog.io/@dbtjr3569</a>
					</div>
				</div>
				<div class="right_contact">
					<div><span class="bold">전화번호</span><a href="">010-8731-8942</a></div>
					<div><a class="infom" href="">이력서바로가기</a></div>
				</div>
			</div>
		</div>
	</section>
</template>
<style scoped>
	.conwrap {
		background-color: #000;
		height: 500px;
	}
	h1 {
		text-align: center;
		color: rgb(255, 255, 255);
		padding-top: 40px;
		font-size: 45px;
		position: relative;
		margin-bottom: 50px;
	}
	h1::after {
		content: '';
		position: absolute;
		left: 47.95%;
		bottom: -2px;
		height: 2px;
		width: 80px;
		background: rgb(255, 255, 255);
	}
	.contact_box {
		display: flex;
		justify-content: space-between;
	}
	.bold {
		font-weight: bold;
		color: aliceblue;
		font-size: 30px;
	}
	.left_contact .s1 {
		padding-left: 275px;
	}
	.left_contact .s2 {
		padding-left: 200px;
	}
	.left_contact > div > a {
		color: rgb(246, 246, 246);
		padding-left: 150px;
		font-size: 20px;
	}
	.contact_box {
		padding: 50px 250px;
	}

	.right_contact > div > a {
		color: rgb(246, 246, 246);
		font-size: 26px;
		padding-left: 20px;
	}
	.right_contact .infom {
		font-size: 30px;
	}
	.left_contact {
		margin-right: 250px;
	}
	.right_contact {
		width: 30%;
	}
	.right_contact > div {
		padding-bottom: 50px;
	}
</style>
