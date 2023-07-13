<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="unsplash__text">
        <h3>Free Image</h3>
        <p>
          unsplash에서는 다양한 이미지를 무료로 제공하고 있습니다.<br />
          다양한 사진들을 무료로 사용하세요!
        </p>
        <router-link to="#" class="button-blue">자세히 보기</router-link>
      </div>
      <div class="unsplash__item">
        <div>
          <router-link to="/"
            ><img src="@/assets/images/unsplash/unsplash01.png" alt="unsplash"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/unsplash/unsplash02.png" alt="unsplash"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/unsplash/unsplash03.png" alt="unsplash"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/unsplash/unsplash04.png" alt="unsplash"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/unsplash/unsplash05.png" alt="unsplash"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/unsplash/unsplash02.png" alt="unsplash"
          /></router-link>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
  },
};
</script>
<style lang="scss">
.unsplash__wrap {
  overflow: hidden;

  .unsplash__inner {
    height: 500px;
    .unsplash__text {
      > h3 {
        font-size: 50px;
        font-weight: 400;
        line-height: 1;
        margin-bottom: 40px;
      }
      > p {
        font-size: 24px;
        font-weight: 300;
        line-height: 1.5;
        margin-bottom: 25px;
      }
      > a {
        border-radius: 50px;
      }
    }

    .unsplash__item {
      padding-top: 70px;
      display: flex;
      position: absolute;
      > div {
        width: 400px;
        margin-right: 27px;

        > a {
          > img {
            border-radius: 10px;
            width: 100%;
            height: 226px;
          }
        }
      }
    }
  }
}
</style>
