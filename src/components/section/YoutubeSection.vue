<template>
  <section id="youtubeSection" :class="attr">
    <div class="youtube__inner container">
      <div class="youtube__text">
        <h3>유튜브 추천</h3>
        <p>재즈 맛집 채널 추천해드립니다</p>
        <router-link to="/" class="button-red">자세히 보기</router-link>
      </div>
      <div class="youtube__item">
        <div>
          <router-link to="/"
            ><img src="@/assets/images/youtube/youtube01.jpg" alt="youtube"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/youtube/youtube02.png" alt="youtube"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/youtube/youtube03.png" alt="youtube"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/youtube/youtube04.png" alt="youtube"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/youtube/youtube05.png" alt="youtube"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/youtube/youtube01.jpg" alt="youtube"
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
// youtube__wrap

.youtube__wrap {
  overflow: hidden;

  .youtube__inner {
    height: 500px;
    .youtube__text {
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

    .youtube__item {
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

.youtube__slider {
  width: 100%;
  a {
    img {
      width: 100%;
      object-fit: cover;
    }
  }
}
.youtube__search {
  text-align: center;
  margin-bottom: 50px;
  margin-top: 50px;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    // @include border(50px);
    min-width: 300px;
    margin-right: 10px;
  }

  button {
    @include button(#f7100d, #fff);
    // @include border(50px)
  }
}
.youtube__tag {
  // display: none

  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;
    li {
      a {
        border: 1px solid #f7100d;
        padding: 10px 20px;
        margin: 0 10px;
        color: #f7100d;
      }
    }
  }
}
.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 24%;
      margin-bottom: 4%;

      img {
        width: 100%;
        object-fit: cover;
      }
      span {
        display: block;
        margin: 4px 0;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        -webkit-line-clamp: 1; /* 라인수 */
      }
    }
  }
}
</style>
