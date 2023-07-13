<template>
  <section id="movieSection" class="movie__wrap section Neo5 bg-vue">
    <div class="movie__inner container">
      <div class="movie__text">
        <h3>추천 영화</h3>
        <p>
          최근 상영작 목록입니다.<br />
          취향에 맞는 영화를 찾으시길 바랍니다.
        </p>
        <router-link to="/" class="button-green">자세히 보기</router-link>
      </div>
      <div class="movie__item">
        <div>
          <router-link to="/"
            ><img src="@/assets/images/movie/movie01.png" alt="movie"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/movie/movie02.png" alt="movie"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/movie/movie03.png" alt="movie"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/movie/movie04.png" alt="movie"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/movie/movie05.png" alt="movie"
          /></router-link>
        </div>
        <div>
          <router-link to="/"
            ><img src="@/assets/images/movie/movie01.png" alt="movie"
          /></router-link>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
.movie__wrap {
  overflow: hidden;

  .movie__inner {
    height: 650px;
    .movie__text {
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

    .movie__item {
      padding-top: 70px;
      display: flex;
      position: absolute;
      > div {
        width: 270px;
        margin-right: 27px;

        > a {
          > img {
            border-radius: 10px;
            width: 100%;
            height: 413px;
          }
        }
      }
    }
  }
}
</style>
