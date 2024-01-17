<template>
  <div class="wrapper" :style="styleVars">
    <background-img />
    <div class="countainer">
      <app-header />

      <div class="body-block">
        <lang-block /> <teacher-main /> <teacher-box />
      </div>
    </div>
    <footer-block />
  </div>
</template>

<script>
import TeacherMain from "./components/TeacherMain.vue";
import AppHeader from "./components/AppHeader.vue";
import BackgroundImg from "./components/BackgroundImg.vue";
import FooterBlock from "./components/FooterBlock.vue";
import LangBlock from "./components/langBlock.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    BackgroundImg,
    LangBlock,
    FooterBlock,
    TeacherMain,
  },
  data() {
    return {
      styleVars: {
        "--violetcolor": "#c05aff",
        "--yellowcolor": "#fffd50",
        "--greencolor": "#c9ff50",
        "--pinkcolor": "#ff50ba",
      },
    };
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Mulish:wght@500;600;800&display=swap");
$fontmain: "Mulish", sans-serif;

* {
  // color: rgb(255, 0, 157);
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: $fontmain;
  font-weight: 500;
}
.wrapper {
  width: 1400px;
  margin: 0 auto;
  position: relative;
  overflow: hidden;
}

ul,
li {
  margin: 0;
  padding: 0;
  list-style: none;
}

.countainer {
  width: 1160px;
  margin: 0 auto;
}
.active {
  color: var(--violetcolor);
}

.body-block {
  display: flex;
  justify-content: space-between;
}
</style>
