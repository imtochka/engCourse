<template>
  <img class="ellipse" src="../assets/img/ellipse.svg" alt="" />
  <img class="lines" src="../assets/img/lines.svg" alt="" />
  <img class="star" src="@/assets/img/star.svg" alt="" />
</template>

<script>
export default {};
</script>

<style scoped>
.ellipse {
  z-index: -1;
  position: absolute;
  width: 335px;
  height: 335px;
  top: 206px;
  left: 1133px;
  transform: rotate(-5.01deg);
}

.lines {
  z-index: -1;
  position: absolute;
  width: 158px;
  height: 244px;
  top: 847px;
  left: 37px;
}
.star {
  z-index: -1;
  position: absolute;
  width: 155px;
  height: 155px;
  top: 889px;
  right: 19px;
  /* bottom: 334px; */
}
</style>
