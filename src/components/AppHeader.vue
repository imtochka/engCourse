<template>
  <div class="headerBlock">
    <div>
      <img src="../assets/img/logo.svg" alt="" />
    </div>
    <div class="headerBlockRight">
      <div>
        <ul class="headerBlockRightListener">
          <li class="active">Курсы</li>
          <li>Статьи</li>
          <li>Вопросы</li>
        </ul>
      </div>

      <div class="headerUserBlock">
        <img src="../assets/img/search.svg" alt="" />
        <img src="../assets/img/user-logo.svg" alt="" />
        <div class="header-lang">
          <p>RU</p>
          <img src="../assets/img/down.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const headerBlockRightListener = document.querySelector(
      ".headerBlockRightListener"
    );
    headerBlockRightListener.addEventListener("click", function (event) {
      console.log(event.target);
      const activeElement = document.querySelector(".active");
      if (activeElement) {
        activeElement.classList.remove("active");
      }
      event.target.classList.add("active");
    });
  },
};
</script>

<style lang="scss">
.headerBlock {
  margin-bottom: 65px;
  margin-top: 40px;
  display: flex;
  justify-content: space-between;
}
.headerBlock div {
  display: flex;
  align-items: center;
}
.headerBlock ul {
  display: flex;
  gap: 70px;
  padding-right: 61px;
  font-size: 18px;
}

.header-lang {
  display: flex;
}
.headerUserBlock {
  gap: 21px;
  display: flex;
}
.header-lang p {
  line-height: 21.6px;
  font-weight: 600;
  font-size: 18px;
  padding-right: 5px;
}
</style>
