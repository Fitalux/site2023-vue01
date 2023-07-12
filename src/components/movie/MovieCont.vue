<template>
  <div className="movie__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a
          :href="`https://www.themoviedb.org/movie/${movie.id}`"
          target="_blank"
        >
          <img
            :src="`https://image.tmdb.org/t/p/w500/${
              movie.poster_path || movie.backdrop_path
            }`"
            :alt="movie.title"
            v-if="movie.poster_path"
          />
          <img
            class="not_poster"
            src="../../assets/images/movie/notPoster.png"
            :alt="movie.title"
            v-else
          />
        </a>
        <em>
          <span className="title">{{ movie.title }}</span>
          <span className="star">{{
            Math.floor(movie.vote_average * 100) / 100
          }}</span>
        </em>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
//movie Cont
.movie__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    font-family: "NanumSquareNeo";

    li {
      width: 24%;
      position: relative;
      margin-bottom: 2%;

      .title {
        font-size: 20px;
        padding: 3px 0;
        display: inline-block;

        &:hover {
          text-decoration: underline;
          text-underline-position: under;
        }
      }

      .star {
        position: absolute;
        right: 20px;
        top: 20px;
        width: 30px;
        height: 30px;
        background-color: #fff;
        text-align: center;
        line-height: 30px;
        border-radius: 50%;
        font-size: 12px;
      }
    }
  }
}
</style>
