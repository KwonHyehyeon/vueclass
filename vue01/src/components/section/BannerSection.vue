<template>
  <section id="bannerType" class="banner__wrap">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">MOMENTO는?</h3>
      <p class="desc">
        트렌드도 중요하지만 한 번 입고 옷장에 박혀있는 옷들 말고<br />
        편안하면서도 오래 입을 수 있는 유행타지 않는 옷들을 추구합니다.
        <a href="#" title="유튜브 페이지로 이동"></a>
      </p>
      <span class="small">-MOMENTO 대표 드림-</span>
    </div>
  </section>
</template>
<style>
.banner__inner {
  background-image: url(../../assets/img/banner_type01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 300;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}
.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}
/* 미디어쿼리 */
@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
