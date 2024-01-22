<template>
  <div class="cart">
    <div class="cart-wrapper">
      <h5>
        Английский шаг за шагом: <span>{{ level }}</span>
      </h5>

      <div class="prise-block">
        <div class="prise-block-top">
          <h6 class="new-prise">2940₽</h6>
          <p class="sail">-51%</p>
        </div>
        <div class="prise-block-bottom">
          <div class="prise-block-bottom-wrapper">
            <p>6000₽</p>
            <div class="line-full-price"></div>
          </div>
        </div>
        <div class="about-course">
          <a href="#">Подробнее</a>

          <svg
            width="18"
            height="18"
            viewBox="0 0 18 18"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0.93934 14.9393C0.353553 15.5251 0.353553 16.4749 0.93934 17.0607C1.52513 17.6464 2.47487 17.6464 3.06066 17.0607L0.93934 14.9393ZM17.5 2C17.5 1.17157 16.8284 0.5 16 0.500001L2.5 0.5C1.67157 0.5 1 1.17157 1 2C1 2.82843 1.67157 3.5 2.5 3.5H14.5V15.5C14.5 16.3284 15.1716 17 16 17C16.8284 17 17.5 16.3284 17.5 15.5L17.5 2ZM3.06066 17.0607L17.0607 3.06066L14.9393 0.93934L0.93934 14.9393L3.06066 17.0607Z"
              fill="#C9FF50"
            />
          </svg>
        </div>
      </div>
    </div>

    <div class="name-block">
      <div class="name-block-text">{{ name }}</div>
      <svg
        class="treangle-mini"
        width="21"
        height="22"
        viewBox="0 0 21 22"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M0.893285 16.9608C0.217188 20.1575 3.45149 22.7724 6.4357 21.4417L18.5443 16.0425C21.2726 14.826 21.7531 11.1568 19.4302 9.27869L10.0649 1.70699C7.7419 -0.171097 4.25471 1.06731 3.6366 3.98987L0.893285 16.9608Z"
        />
      </svg>
    </div>

    <img class="backgroundImg" :src="imageUrlBack" alt="" />
    <img class="personImg" :src="imageUrlPerson" alt="" />
    <img class="flag-img" src="/src/assets/img/english-flag.svg" alt="" />
  </div>
</template>

<script>
import SvgImage from "../assets/img/treangle.svg";

export default {
  data() {
    return { svgImage: SvgImage };
  },

  props: {
    name: {
      type: String,
      required: true,
    },
    backImg: {
      type: String,
      required: true,
    },
    level: {
      type: String,
      required: true,
    },

    personImg: {
      type: String,
      required: true,
    },

    personImgUrl: null,
  },
  methods: {},
  computed: {
    imageUrlBack() {
      console.log(`/src/assets/img/${this.backImg}.svg`);
      return new URL(`/src/assets/img/${this.backImg}.svg`, import.meta.url)
        .href;
    },
    imageUrlPerson() {
      console.log(`/src/assets/img/${this.personImg}.svg`);
      return new URL(`/src/assets/img/${this.personImg}.svg`, import.meta.url)
        .href;
    },
  },
};
</script>

<style scoped>
.about-course {
  justify-content: right;
  float: right;
  display: inline-flex;
}

.about-course a {
  text-decoration: none;
  color: white;
  font-size: 18px;
  font-weight: 500px;
  padding-right: 5px;
  padding-bottom: 2px;
}

.line-full-price {
  width: 100%;
  height: 1px;
  background-color: var(--pinkcolor);
  position: absolute;
  z-index: 5;
  align-self: center;
}

.prise-block-bottom {
  display: flex;
  justify-content: right;
  margin-right: 32px;
  margin-bottom: 37px;
}
.prise-block-bottom p {
  font-weight: 800;
  font-size: 20px;
  color: white;
}
.sail {
  display: inline-flex;
  padding: 3px 11px;
  font-weight: 600;
  font-size: 10px;
  background-color: var(--pinkcolor);
  align-self: flex-end;
  border-radius: 20px;
  color: white;
}
.prise-block {
  position: relative;
  z-index: 1;

  display: flex;
  flex-direction: column;
  float: right;
}
.prise-block h6 {
  font-weight: 800;
  font-size: 40px;
  line-height: 48px;
  color: #ffffff;
}
.prise-block-top {
  gap: 9px;
  display: flex;
  justify-content: right;
}
.treangle-mini {
  fill: var(--greencolor);
}
.cart {
  display: flex;
  position: relative;
  padding: 24px 22px;
  background-color: rgba(255, 0, 0, 0.168);
  width: 400px;
  height: auto;
  border-radius: 30px;
}
.cart {
  background-color: var(--violetcolor);
}
.cart-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
h5 {
  position: relative;
  z-index: 2;
  font-size: 24px;
  font-weight: 800;
  color: #ffffff;
  margin-bottom: 101px;
  line-height: 28.8px;
}
span {
  color: var(--yellowcolor);
}
.flag-img {
  z-index: 2;
  position: absolute;
  bottom: 11px;
  left: 144px;
  width: 66px;
  height: 66px;
}
.name-block {
  margin-left: 126px;
  bottom: 208px;
  position: absolute;
}
.name-block svg {
  position: absolute;
  left: -13px;
  bottom: -18px;
  z-index: 2;
}
.name-block-text {
  position: relative;
  z-index: 2;
  padding: 6px 18px;
  background-color: var(--greencolor);
  border-radius: 60px;
  display: inline-flex;
}
.prise-block-bottom-wrapper {
  position: relative;
  display: inline-flex;
}
.background-img-wrapper {
  position: relative;
  bottom: 120px;
}
.backgroundImg {
  position: absolute;
  right: 30px;
  bottom: 142px;
}
.personImg {
  z-index: 1;
  position: absolute;
  bottom: 0;
  left: 0;
}
</style>
