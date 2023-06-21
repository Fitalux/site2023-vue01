<template>
  <footer id="footer" class="footer__wrap Neo5 bg-blue" role="contentinfo">
    <div class="footer__inner container">
      <div class="footer__text">
        <h5>Fitelux</h5>
        <p>
          궁금한 사항은 메일로 연락 주세요. <br />
          <a href="mailto:sehen0422@naver.com">sehen0422@naver.com</a>
        </p>
        <ul class="sns">
          <li>
            <a href="/"><span class="ir">Git Hub</span></a>
          </li>
          <li>
            <a href="/"><span class="ir">Blog</span></a>
          </li>
          <li>
            <a href="/"><span class="ir">CodePen</span></a>
          </li>
          <li>
            <a href="/"><span class="ir"></span></a>
          </li>
        </ul>
      </div>
      <div class="footer__menu">
        <div>
          <h4>Site</h4>
          <ul>
            <li>
              <a href="/">웹표준 사이트<br />(Web Standard Site)</a>
            </li>
            <li><a href="/">반응형 사이트</a></li>
            <li><a href="/">패럴렉스 사이트</a></li>
            <li><a href="/">포트폴리오 사이트</a></li>
          </ul>
        </div>
        <div>
          <h4>유형</h4>
          <ul>
            <li><a href="/">이미지 유형</a></li>
            <li><a href="/">카드 유형</a></li>
            <li><a href="/">이미지/텍스트 유형</a></li>
            <li><a href="/">배너 유형</a></li>
            <li><a href="/">텍스트 유형</a></li>
            <li><a href="/">푸터 유형</a></li>
          </ul>
        </div>
        <div>
          <h4>SCRIPT</h4>
          <ul>
            <li><a href="/">Search Effect</a></li>
            <li><a href="/">Slider Effect</a></li>
            <li><a href="/">Mouse Effect</a></li>
            <li><a href="/">Quiz Effect</a></li>
            <li><a href="/">Parallax Effect</a></li>
            <li><a href="/">Game Effect</a></li>
          </ul>
        </div>
        <div>
          <h4>Reference</h4>
          <ul>
            <li><a href="/">CSS</a></li>
            <li><a href="/">FONTS</a></li>
            <li><a href="/">HTML</a></li>
            <li><a href="/">JAVASCRIPT</a></li>
            <li><a href="/">REACT</a></li>
          </ul>
        </div>
      </div>
      <div class="footer__right">
        Copyright 2023. All Rights Reserved. - Designed by Fita Lux
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
.footer__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  .footer__text {
    width: 20%;
    margin-top: 20px;

    h5 {
      font-size: 20px;
      margin-bottom: 20px;
    }
    p {
      font-size: 16px;
      color: #666;
    }
    .sns {
      li {
        display: inline;
        a {
          display: inline-block;
          width: 45px;
          height: 45px;
          border-radius: 50px;
          background-image: url(../../assets/images/footer_icon.svg);
        }
        &:nth-child(2) a {
          background-position: -45px 0;
        }
        &:nth-child(3) a {
          background-position: -90px 0;
        }
        &:nth-child(4) a {
          background-position: -135px 0;
        }
      }
    }
  }

  .footer__menu {
    margin-top: 20px;
    width: 70%;
    display: flex;

    > div {
      width: 25%;

      h4 {
        font-size: 18px;
        color: #000;
        margin-bottom: 20px;
      }

      a {
        font-size: 14px;
        color: #666;
        line-height: 1.8;
      }
    }
  }

  .footer__right {
    width: 100%;
    padding: 30px;
    text-align: center;
    border-top: 1px solid #fcfcfc;
    margin-top: 50px;
    color: #666;
    font-size: 14px;
  }
}
</style>
