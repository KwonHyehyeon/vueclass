<template>
  <section id="imageTextType" class="imageText__wrap" :class="attr">
    <h2 class="blind">다가오는 가을 코디 추천</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <span>{{ titles[0].smalltitle }}</span>
        <h3>
          {{ titles[0].title1 }} <br />
          {{ titles[0].title2 }}
        </h3>
        <p>{{ titles[0].desc }}</p>
        <ul>
          <li v-for="text in texts" v-bind:key="text">
            <a href="#">{{ text }}</a>
          </li>
        </ul>
      </div>
      <div
        class="imgText__img"
        v-for="img in imgs"
        v-bind:key="img.img"
        :class="img.img"
      >
        <a href="#">{{ img.desc }}</a>
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
  data: function () {
    return {
      titles: [
        {
          smalltitle: "MOMENTO’s pick",
          title1: "다가오는",
          title2: "가을 코디 추천",
          desc: "모멘토가 pick한 가을 색감 뿜뿜 코디 추천 지금 바로 공개합니다!",
        },
      ],
      texts: [
        "셔츠 + 핀턱 슬랙스 + 로퍼/운동화",
        "니트 + 골덴 숏팬츠 + 부츠",
        "가디건 + 반팔 티셔츠 + 팬츠",
        "캡모자 + 쉬폰 원피스 + 운동화",
        "라이더 자켓 + 반팔 티셔츠 + 팬츠",
        "트렌치코트 + 티셔츠 + 면팬츠",
      ],
      imgs: [
        {
          img: "img1",
          desc: "초가을 코디 보러가기",
        },
        {
          img: "img2",
          desc: "늦가을 코디 보러가기",
        },
      ],
    };
  },
};
</script>

<style>
/* imageTextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
}
.imgText__inner > div {
  width: 32%;
  height: 500px;
}
.imgText__txt span {
  font-size: 16px;
  color: #666;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
  display: block;
}
.imgText__txt h3 {
  font-size: 50px;
  font-weight: 300;
  margin-bottom: 20px;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #666;
  margin-bottom: 10px;
}
.imgText__txt ul {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.6;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #666;
}
.imgText__txt ul li::before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: #7c2b39;
  color: #fff;
  font-size: 18px;
  padding: 10px 30px;
  border-radius: 30px;
  display: inline-block;
}
.imgText__img a.blue {
  background-color: #784c23;
}
.imgText__img.img1 {
  background: url(../../assets/img/imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgText_bg02.jpg) no-repeat center / cover;
}

/* 미디어쿼리 */
@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 40px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__txt {
    width: 100%;
    /* height값 초기화 */
    height: auto;
    text-align: center;
  }
  .imgText__inner > div.imgText__txt ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 49%;
  }
}

@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 200px;
  }
  .imgText__inner > div.imgText__img {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}
</style>
