<template>
  <div class="teacher-block">
    <h1>Курсы<span>английского языка</span></h1>
    <!-- <div class="teacherBlockCarts">
      <div class="teacherBlockCartsLeft"><teacher-cart /> <teacher-cart /></div>
      <div class="teacherBlockCartsRight">
        <teacher-cart /> <teacher-cart />
      </div>
    </div> -->
    <div class="cart-sort">
      <div v-for="item in items" :key="item.id">
        <teacher-cart
          :name="item.name"
          :level="item.level"
          :personImg="item.personImg"
          :newPrise="item.newPrise"
          :oldPrise="item.oldPrise"
          :backImg="item.backImg"
        />
      </div>
    </div>
  </div>
</template>

<script>
import TeacherCart from "./TeacherCart.vue";
export default {
  components: { TeacherCart },
  data() {
    return {
      items: [
        {
          id: 1,
          name: "Полина Коваленко",
          backImg: "az",
          personImg: "girl1",
          level: "Базовый уровень",
        },
        {
          id: 2,
          name: "Не Полина Коваленко",
          backImg: "ae",
          backImgTwo: "az",
          personImg: "girl2",
          level: "Вводно-фонетический курс",
        },

        {
          id: 3,
          name: "Точно Полина Коваленко",
          backImg: "az",
          personImg: "girl1",
          level: "Другой курс",
        },
        {
          id: 4,
          name: "Полина Коваленко",
          backImg: "ae",
          personImg: "girl2",
          level: "Еще один другой курс",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.cart-sort {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 60px;
  grid-row-gap: 30px;
}
// .qwe {
//   display: flex;
//   flex-direction: row;
//   margin-bottom: 30px;
// }
// .qwe div {
//   margin-left: 53px;
// }
h1 {
  font-weight: 800;
  font-size: 48px;
  margin-bottom: 73px;
}
span {
  font-weight: 800;
  font-size: 48px;
  padding: 7px 14px 14px 14px;
  background-color: var(--greencolor);
  border-radius: 100px;
}
.teacherBlockCarts {
  display: flex;
  justify-content: space-between;
}
.teacherBlockCartsLeft {
  display: flex;
  flex-direction: column;
  margin-right: 53px;
  gap: 30px;
}

.teacherBlockCartsRight {
  display: flex;
  gap: 30px;
  flex-direction: column;
}
</style>
