<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>이 달의 마켓</h2>
    <p>MOMENTO’s가 pick해 온 의류 품목들을 공개합니다.</p>
    <div class="card__inner" :class="layout">
      <article class="card">
        <!--시맨틱태그 안에는 제목이 꼭 들어가야함!-->
        <figure class="card__header">
          <!--이미지 가져오는 새로운 기능-->
          <img src="../../assets/img/card_bg01.jpg" alt="코듀로이 팬츠" />
          <!--웹표준 준수하기 위함으로 alt적어주는 것 접근성을 향상 시키기 위함-->
        </figure>
        <div class="card__body">
          <h3 class="tit">코듀로이 팬츠</h3>
          <p class="desc">
            가을하면 코듀로이, 코듀로이하면 가을로 그만큼 대표적인 가을 소재라고
            할 수 있는 코듀로이 팬츠를 가져왔습니다. 요즘 팬츠 색상이 다양한 게
            트렌드인 만큼 여러 색상을 가져왔는데.........
          </p>
          <a class="btn" href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg02.jpg" alt="코끼리" />
        </figure>
        <div class="card__body">
          <h3 class="tit">블라우스</h3>
          <p class="desc">
            가을하면 빠질 수 없는 블라우스도 가져왔는데 여리여리 느낌을 줄 수
            있는 블라우스를 가져오고 싶어서 레이스가 포인트인 블라우스를
            가져왔습니다. 구김이 잘 가지 않는 소재로 데려왔......
          </p>
          <a class="btn" href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg03.jpg" alt="돌고래" />
        </figure>
        <div class="card__body">
          <h3 class="tit">트렌치 코트</h3>
          <p class="desc">
            가을하면 모두 트렌치 코트를 떠올리시잖아요? 그래서 가져왔습니다.
            자칫하면 촌스러워보일 수 있는 색감의 트렌치코트는 제외하고 탄탄하고
            오래 입을 수 있는 트렌치코트로 데려왔습니다.
          </p>
          <a class="btn" href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
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
};
</script>
<style>
/* cardType */
.card__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  /*양쪽 정렬 맞춰주는 것*/
}

.card {
  width: 32%;
  background: #f5f5f5;
}

.card__body {
  padding: 24px;
}

.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  /* 한 줄 효과 */
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4; /*줄효과 clamp : 4줄 효과*/
  -webkit-box-orient: vertical;
}
.card__body .btn:hover {
  text-decoration: underline;
}
/* 미디어쿼리 */
@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
}
</style>
