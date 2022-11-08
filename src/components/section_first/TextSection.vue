<template>
  <section id="textType" class="text__wrap" :class="attr">
    <!-- 쓸 거 없을 때 div나 span -->
    <span>MOMENTO’s</span>
    <h2 class="mb70">SNS : MOMENTO’s LOOK</h2>
    <div class="text__inner" :class="layout">
      <div class="text t1">
        <h3 class="text__title">페이스북</h3>
        <p class="text__desc">
          MOMENTO의 룩북영상과 홍보영상을 볼 수 있으며 매달 마켓 상품 품목들을
          실시간으로 확인하실 수 있습니다.
        </p>
        <a class="text__btn" href="#">바로가기</a>
      </div>
      <div class="text t2">
        <h3 class="text__title">인스타</h3>
        <p class="text__desc">
          MOMENTO의 실시간 라이브 영상을 볼 수 있으며 고객님들의 리뷰사진을
          스토리에 공유합니다.
        </p>
        <a class="text__btn" href="#">바로가기</a>
      </div>
      <div class="text t3">
        <h3 class="text__title">유튜브</h3>
        <p class="text__desc">
          MOMENTO의 실시간 라이브 영상을 볼 수 있으며 촬영 비하인드 영상도 볼 수
          있습니다. 그 외의 영상 계획도 있습니다.
        </p>
        <a class="text__btn" href="#">바로가기</a>
      </div>
      <div class="text t4">
        <h3 class="text__title">카카오톡</h3>
        <p class="text__desc">
          MOMENTO의 CS를 맡고 있으며 문의를 하고 싶으실 때 카카오톡을 통해
          문의를 주시면 신속하게 답변하고 있습니다.
        </p>
        <a class="text__btn" href="#">바로가기</a>
      </div>
      <div class="text t5">
        <h3 class="text__title">트위터</h3>
        <p class="text__desc">
          MOMENTO 신상컷들을 업데이트 하고 있으며 업데이트 소식을 보다 빠르게
          확인 할 수 있습니다.
        </p>
        <a class="text__btn" href="#">바로가기</a>
      </div>
      <div class="text t6">
        <h3 class="text__title">네이버 블로그</h3>
        <p class="text__desc">
          MOMENTO 공지사항이나 이벤트 소식 등을 전달하는 곳입니다. 추후에 진행할
          플리마켓 공지도 여기서 확인할 수 있습니다.
        </p>
        <a class="text__btn" href="#">바로가기</a>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>
<style>
/* textType */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  /* background: #f5f5f5; */
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #f5f5f5;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: #000;
  background: url(../../assets/img/textIcon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text__btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}
/* 미디어쿼리 */
@media (max-width: 960px) {
  .text {
    width: 49%;
    background: #f5f5f5;
  }
}

@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}
@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
