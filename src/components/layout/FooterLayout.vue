<template>
  <footer id="footerType" class="footer__wrap" :class="attr">
    <h2 class="blind">푸터 영역</h2>
    <div class="footer__inner" :class="layout">
      <div class="footer__menu">
        <div>
          <h3>MENU</h3>
          <ul>
            <li>
              <a href="/">OUTER</a>
            </li>
            <li>
              <a href="/">TOP</a>
            </li>
            <li>
              <a href="/">BOTTOM</a>
            </li>
            <li>
              <a href="/">DRESS</a>
            </li>
            <li>
              <a href="/">ACC</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>SHOP GUIDE</h3>
          <ul>
            <li>
              <a href="/">이용 약관</a>
            </li>
            <li>
              <a href="/">이용 안내</a>
            </li>
            <li>
              <a href="/">개인정보취급방침</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>MEMBERSHIP</h3>
          <ul>
            <li>
              <a href="/">로그인</a>
            </li>
            <li>
              <a href="/">회원가입</a>
            </li>
            <li>
              <a href="/">마이페이지</a>
            </li>
            <li>
              <a href="/">주문조회</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>BANK ACCOUNT</h3>
          <ul>
            <li>
              <a href="/">신한 : 123-4567-890</a>
            </li>
            <li>
              <a href="/">예금주 : (주)모멘토컴퍼니 </a>
            </li>
          </ul>
        </div>
        <div>
          <h3>ABOUT US</h3>
          <ul>
            <li>
              <a href="/">company.(주)모멘토컴퍼니</a>
            </li>
            <li>
              <a href="/">owner. 권혜현</a>
            </li>
            <li>
              <a href="/">tel. 031-123-4567</a>
            </li>
            <li>
              <a href="/">business no. 123-45-67</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>SNS</h3>
          <ul>
            <li>
              <a href="/">페이스북</a>
            </li>
            <li>
              <a href="/">인스타</a>
            </li>
            <li>
              <a href="/">유튜브</a>
            </li>
            <li>
              <a href="/">카카오톡</a>
            </li>
            <li>
              <a href="/">트위터</a>
            </li>
            <li>
              <a href="/">네이버 블로그</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__right">
        2022 NOEYHEYH. This is hyeon's Portfolio
        <br />
        All rights reserved.
      </div>
    </div>
  </footer>
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
.footer__inner {
  width: 85%;
  padding: 0 20px;
  margin: 0 auto;
}
.footer__menu {
  display: flex;
  /* flex-wrap: wrap; */
  justify-content: space-between;
  margin-bottom: 70px;
}
.footer__menu h3 {
  font-size: 18px;
  margin-bottom: 20px;
}
.footer__menu li a {
  font-size: 14px;
  color: #666;
  margin-bottom: 10px;
  display: block;
}
.footer__right {
  border-top: 1px solid #d9d9d9;
  text-align: center;
  padding-top: 48px;
  color: #666;
  line-height: 1.5;
}
/* 반응형 */
@media (max-width: 960px) {
  .footer__menu {
    display: none;
  }
  .footer__right {
    padding-top: 0;
    border-top: 0;
  }
  .footer__wrap {
    padding: 40px 0;
  }
}
</style>
