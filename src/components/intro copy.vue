<template>
  <section id="Intro" class="main">
    <div class="rolling_box">
      <ul id="rolling_box">
        <li
          v-for="(test, index) in rollingData"
          :key="index"
          :id="test.id"
          class="card_sliding"
        >
          <p>{{ test.test1 }}</p>
        </li>
      </ul>
    </div>
    <div class="text-box">
      <h1 class="h1">개발자 <span>김유석</span>입니다 :)</h1>
      <p class="sp">2023 PORTFOLIO</p>
    </div>
  </section>
</template>
<script>
import { ref } from "vue";
export default {
  setup() {
    const rollingData = [
      { test1: "성장 하고 싶은", id: "first" },
      { test1: "꾸준 하고 싶은", id: "second" },
      { test1: "발전 하고 싶은", id: "third" },
    ]; //
    let move = ref(2);
    const test = () => {
      const first = document.getElementById("first");
      const second = document.getElementById("second");
      const third = document.getElementById("third");

      if (move.value == 2) {
        first.classList.remove("card_sliding");
        first.classList.add("card_sliding_after");

        second.classList.remove("card_sliding_after");
        second.classList.add("card_sliding");

        third.classList.remove("card_sliding_after");
        third.classList.remove("card_sliding");

        move.value = 0;
      } else if (move.value == 0) {
        first.classList.remove("card_sliding_after");
        first.classList.remove("card_sliding");

        second.classList.remove("card_sliding");
        second.classList.add("card_sliding_after");

        third.classList.remove("card_sliding_after");
        third.classList.add("card_sliding");

        move.value = 1;
      } else if (move.value == 1) {
        first.classList.remove("card_sliding_after");
        first.classList.add("card_sliding");

        second.classList.remove("card_sliding_after");
        second.classList.remove("card_sliding");

        third.classList.remove("card_sliding");
        third.classList.add("card_sliding_after");

        move.value = 2;
      }
    };
    setInterval(() => {
      test();
    }, 3000);

    return {
      rollingData,
      move,
    };
  },
};
</script>
<style scoped>
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

.rolling_box {
  width: 1000px;
  height: 100px;
  position: absolute;
  top: 20%;
}

.rolling_box ul {
  width: 100%;
  height: 100%;
  overflow: hidden;
  position: relative;
}
.rolling_box ul li {
  width: 100%;
  height: 100%;
  transition: 0.9s;
  position: absolute;
  transition: top 0.7s;
  top: 130%;
  z-index: 1;
}

.rolling_box ul li.card_sliding {
  top: 20px;
}

.rolling_box ul li.card_sliding_after {
  top: 40px;
}

.rolling_box ul li p {
  font-size: 70px;
  line-height: 70px;
  color: #fff;
  text-align: center;
}
.card_sliding {
  top: 0 !important;
  z-index: 100 !important;
}
.card_sliding_after {
  top: -100% !important;
  z-index: 10 !important;
}

/* .before_slide {
  transform: translateY(100%);
}

.after_slide {
  transform: translateY(0);
} */
</style>
