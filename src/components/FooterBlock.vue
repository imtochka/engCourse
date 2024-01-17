<template>
  <div class="footer">
    <div class="countainer">
      <div class="footer-block-top">
        <div class="footer-block-top-left">
          <p>Политика конфиденциальности</p>
          <p>Условия пользования</p>
        </div>
        <div><img src="../assets/img/logo-white.svg" alt="" /></div>
      </div>
      <p class="footer-block-bottom">© DailyLangs | 2023. Все права защищены</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  background-color: var(--violetcolor);
  height: auto;
  padding: 55px 0 45px 0;
  width: 1400px;
  margin: 0 auto;
  margin-top: 140px;
}
.footer-block-top {
  color: white;
  display: flex;
  justify-content: space-between;
  margin-bottom: 52px;
}
.footer-block-top-left {
  display: flex;
  flex-direction: column;
  gap: 13px;
  font-size: 18px;
}
.footer-block-bottom {
  color: white;
  text-align: center;
  font-size: 18px;
}
</style>
