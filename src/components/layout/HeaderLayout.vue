<template>
  <header id="headerType" :class="fonts">
    <div class="header__inner">
      <div class="header__logo">
        <a href="/"> MOMENTO <em>store</em> </a>
      </div>
      <div class="header__menu">
        <ul>
          <li>
            <a href="#sliderType">main</a>
          </li>
          <li>
            <a href="#imageType">best</a>
          </li>
          <li>
            <a href="#imageTextType">codi</a>
          </li>
          <li>
            <a href="#cardType">product</a>
          </li>
          <li>
            <a href="#bannerType">brand</a>
          </li>
          <li>
            <a href="#textType">SNS</a>
          </li>
        </ul>
      </div>
      <div class="header__member">
        <a href="/">로그인</a>
      </div>
      <div class="header__ham">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    fonts: String,
  },
};
</script>

<style>
/* headerType */
.header__inner {
  width: 100%;
  height: 70px;
  display: flex;
  /* flex-wrap: wrap; */
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  box-sizing: border-box;
  border-bottom: 1px solid #ccc;
  position: fixed;
  left: 0;
  top: 0;
  z-index: 10000;
  background: #fff;
  backdrop-filter: blur(10px);
}
.header__logo {
  width: 20%;
  font-size: 30px;
  font-weight: 700;
  text-transform: uppercase;
}
.header__logo em {
  font-size: 18px;
  font-weight: 400;
  color: #999;
}
.header__menu {
  width: 60%;
  /* background: #fff; */
  text-align: center;
}
.header__menu li {
  display: inline;
}
.header__menu li a {
  padding: 12px 30px;
  margin: 0 10px;
  transition: background-color 0.3s;
}
.header__menu li a:hover {
  background-color: #e4b88e81;
  color: #fff;
  border-radius: 5px;
}
.header__menu ul li.active a {
  background-color: #e4b78e;
  color: #fff;
  border-radius: 5px;
}
.header__member {
  width: 20%;
  text-align: right;
}
.header__member a {
  font-size: 16px;
  border: 1px solid #000;
  padding: 10px 30px;
  border-radius: 50px;
  transition: all 0.3s;
}
.header__member a:hover {
  background-color: #000;
  color: #fff;
}
.header__ham {
  position: absolute;
  right: 16px;
  top: 10px;
  z-index: 1000;
  width: 50px;
  height: 50px;
  /* background: blue; */
  display: none;
  cursor: pointer;
}
.header__ham span {
  display: block;
  background: #000;
  width: 30px;
  height: 2px;
  border-radius: 3px;
  margin-left: 10px;
  margin-top: 5px;
  transition: 0.25s margin 0.25s, 0.25s transform;
}
.header__ham span:nth-child(1) {
  margin-top: 17px;
}
.header__ham.active span {
  /* 가운데 0.25s는 딜레이 */
  transition: 0.25s margin, 0.25s transform 0.25s;
}
.header__ham.active span:nth-child(1) {
  margin-top: 25px;
  margin-bottom: -7px;
  transform: rotate(45deg);
}
.header__ham.active span:nth-child(2) {
  transform: rotate(45deg);
}
.header__ham.active span:nth-child(3) {
  margin-top: -2px;
  transform: rotate(135deg);
}

/* 미디어쿼리 */
@media (max-width: 1300px) {
  .header__menu {
    position: fixed;
    right: -100%;
    top: 69px;
    background: #fff;
    width: 60%;
    height: 100vh;
    padding: 20px;
    text-align: right;
    transition: right 0.4s ease-in;
  }
  .header__menu ul li {
    display: block;
    margin: 20px;
  }
  .header__menu ul li a {
    padding: 10px;
    white-space: nowrap;
  }
  .header__menu.active {
    right: 0;
  }
  .header_logo {
    width: 50%;
  }
  .header__member {
    margin-right: 50px;
    width: 30%;
    font-size: 10px;
  }
  .header__ham {
    display: block;
  }
}
</style>
