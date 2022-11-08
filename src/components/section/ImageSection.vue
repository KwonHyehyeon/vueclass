<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>{{ titles[0].title }}</h2>
    <p>{{ titles[0].desc }}</p>
    <div class="image__inner" :class="layout">
      <article
        class="image"
        v-for="img in imgs"
        v-bind:key="img.img"
        :class="img.img"
      >
        <h3 class="image__title">{{ img.title }}</h3>
        <p class="image__desc">
          {{ img.desc }}
        </p>
        <a class="image__btn green" href="/" title="상세 보기">상세 보기</a>
      </article>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
data: function () {
    return {
      titles: [
        {
          title: "이 달의 BEST",
          desc: "9월 가장 인기가 많았던 제품 TOP 2 를 지금 바로 소개합니다.",
        },
      ],
      imgs: [
        {
          img: "img1",
          title: "brin tweed jacket",
          desc: '“브린 트위드 자켓" 은 화이트톤과 아이보리 톤의 조화로 체크무늬가 들어간 자켓으로, 하객룩으로 인기가 많은 제품입니다.',
        },
        {
          img: "img2",
          title: "cross denim pants",
          desc: '“크로스 데님 팬츠" 는 사선 버튼이 포인트인 청바지로 요즘 대세인 와이드 형태의 팬츠입니다. 사계절 내내 착용하실 수 있습니다.',
        },
      ],
    };
  },
};
</script>
<style>
/* imageType */
.image__wrap {
}
.image__wrap h2 {
}
.image__wrap p {
} /*section의 요소들과 같아서 section에 넣어줌(코드 재활용을 위해서)*/
#imageType01 {
  /* height: 500px; */
}
.image__wrap {
}
.image__inner {
  display: flex;
  /* flex-wrap: wrap; */
  justify-content: space-between; /*컨테이너 있고 이거쓰면 양쪽 끝으로 붙어서 사진 사이 떨어지게 함*/
}
.image {
  width: 49%;
  height: 370px;
  padding: 200px 30px 30px 30px; /*글씨 옮기려고 넣는것*/
  box-sizing: border-box; /*패딩을 쓰면 그만큼 커지기 때문에 이를 방지하는 것*/
  color: #fff;
}
.image.img1 {
  background: url(../../assets/img/img01.jpg) no-repeat center / cover;
}
.image.img2 {
  background: url(../../assets/img/img02.jpg) no-repeat center / cover;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  /* 한줄효과 */
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 16px;
  margin-bottom: 10px;
  line-height: 1.4;
  font-weight: 300;
  padding-right: 100px;
  overflow: hidden;
  text-overflow: ellipsis; /*텍스트 흘렀을 때 ...으로 바꿔줌*/
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  margin-bottom: 10px;
}
.image__btn {
  font-size: 16px;
  font-weight: 300;
  background: #626262;
  color: #fff;
  padding: 10px 20px;
  display: inline-block;
}
.image__btn.green {
  background: #1a4272;
}
/* 미디어쿼리 */
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 205px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
  .image__desc {
    font-size: 16px;
  }
}
</style>
