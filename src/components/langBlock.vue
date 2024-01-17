<template>
  <div class="langBlock">
    <div class="langBlockBtn">
      <p>Язык</p>
      <img src="../assets/img/down-white.svg" alt="" />
    </div>

    <h5>Продолжительность</h5>
    <div class="sliderBlock">
      <p>От {{ minValue }} до {{ maxValue }} мес.</p>
      <div class="slider">
        <div class="slider-dot slider-dot-min"></div>
        <div class="slider-line"></div>
        <div class="slider-dot slider-dot-max"></div>
      </div>
    </div>
    <h5>Сложность</h5>
    <div class="radioCircle">
      <span>
        <label class="custom-radio">
          <input type="radio" name="custom-radio" checked />
          <span class="radio-dot"></span>
        </label>
        <p>Для всех</p></span
      >

      <span>
        <label class="custom-radio">
          <input type="radio" name="custom-radio" />
          <span class="radio-dot"></span>
        </label>
        <p>Продвинутый уровень</p></span
      >

      <span>
        <label class="custom-radio">
          <input type="radio" name="custom-radio" />
          <span class="radio-dot"></span>
        </label>
        <p>Для всех</p></span
      >
    </div>
    <h5>Навыки</h5>
    <div class="radioSquare">
      <span>
        <label class="custom-radio-btn">
          <input type="radio" name="custom-radio-two" />
          <span class="radio-square"></span>
        </label>
        <p>Грамматика</p> </span
      ><span>
        <label class="custom-radio-btn">
          <input type="radio" name="custom-radio-two" />
          <span class="radio-square"></span>
        </label>
        <p>Лексика</p> </span
      ><span>
        <label class="custom-radio-btn">
          <input type="radio" name="custom-radio-two" />
          <span class="radio-square"></span>
        </label>
        <p>Синтаксис</p> </span
      ><span>
        <label class="custom-radio-btn">
          <input type="radio" name="custom-radio-two" />
          <span class="radio-square"></span>
        </label>
        <p>Фонетика</p> </span
      ><span>
        <label class="custom-radio-btn">
          <input type="radio" name="custom-radio-two" />
          <span class="radio-square"></span>
        </label>
        <p>Продвинутый уровень</p>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      maxValue: 6,
      minValue: 1,
      options: [1, 2, 3, 4, 5, 6],
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
h5 {
  font-weight: 600;
  font-size: 18px;
  margin-bottom: 30px;
}

p {
  font-weight: 500;
  font-size: 18px;
}
.radioCircle {
  margin-bottom: 30px;
  display: flex;
  flex-direction: column;
  gap: 11px;
}
.radioCircle span {
  display: flex;
  align-items: center;
}
//// КРУГЛЫЕ
.custom-radio {
  display: inline-block;
  position: relative;
  cursor: pointer;
  margin-right: 10px;
}

.custom-radio input[type="radio"] {
  opacity: 0;
  position: absolute;
  top: 0;
  left: 0;
}

.custom-radio .radio-dot {
  display: inline-block;
  width: 14px;
  height: 14px;
  border: 1px solid var(--violetcolor);
  // border-color: --violetcolor;
  border-radius: 50%;
  transition: background-color 0.2s;
}

.custom-radio input[type="radio"]:checked + .radio-dot {
  background-color: var(--violetcolor);
}
////////КВАДРАТНЫЕ
.custom-radio-btn {
  display: inline-block;
  position: relative;
  width: 14px;
  height: 14px;
}

.custom-radio-btn input[type="radio"] {
  position: absolute;
  opacity: 0;
}

.custom-radio-btn .radio-square {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 1px solid var(--violetcolor);
  border-radius: 2px;
  cursor: pointer;
  transition: background 0.2s;
}

.custom-radio-btn input[type="radio"]:checked + .radio-square {
  background-color: var(--violetcolor);
}
.radioSquare {
  display: flex;
  flex-direction: column;
  gap: 11px;
}
.radioSquare span {
  display: flex;
  align-items: center;
  gap: 12px;
}
///

.langBlock {
}
.langBlockBtn {
  border-radius: 100px;
  display: inline-flex;
  padding: 15px 60px;
  background-color: var(--violetcolor);
  margin-bottom: 76px;
  color: #ffffff;
  font-weight: 600;
  font-size: 18px;
  gap: 18px;
}
.langBlockBtn img {
  fill: white;
}

.slider {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.slider {
  width: 190px;
  height: 1px;
  background-color: var(--violetcolor);
}
.sliderBlock {
  margin-bottom: 37px;
}
.sliderBlock p {
  margin-bottom: 10px;
}
.slider-dot {
  width: 13.2px;
  height: 14px;
  border-radius: 50%;
  background-color: var(--violetcolor);
}
</style>
