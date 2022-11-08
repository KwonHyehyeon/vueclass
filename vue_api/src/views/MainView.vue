<template>
  <div>
    <HeaderCont />
    <section class="main__cont">
      <div class="container">
        <div class="main__inner">
          <!-- 밑에 데이터 불러오기 (반복문 사용)-->
          <div v-for="title in titles" v-bind:key="title.text">
            {{ title.text }}
          </div>
          <!-- <div>we provide</div>
          <div>visual coding</div>
          <div>solutions</div>
          <div>for you API</div> -->
        </div>
      </div>
    </section>
    <FooterCont />
  </div>
</template>

<script>
import HeaderCont from "@/components/HeaderCont.vue";
import FooterCont from "@/components/FooterCont.vue";

export default {
  components: {
    HeaderCont,
    FooterCont,
  },
  // 함수만들려면 이 사이에 있어야 함
  data: function () {
    return {
      titles: [
        { text: "we provide" },
        { text: "visual coding" },
        { text: "solutions" },
        { text: "for you API" },
      ],
    };
  },
};
</script>

<style lang="scss">
.main__inner {
  display: flex;
  justify-content: center;
  align-items: start;
  flex-direction: column;
  height: 100vh;
  color: var(--black);

  > div {
    font-size: 9.4vw;
    line-height: 0.9;
    text-transform: uppercase;
  }
}
</style>
