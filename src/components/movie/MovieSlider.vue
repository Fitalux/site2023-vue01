<template>
  <div className="movie__slider">
    <swiper
      :modules="modules"
      :slides-per-view="2"
      :spaceBetween="3"
      :pagination="{ clickable: true }"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 3000 }"
    >
      <swiper-slide v-for="(movie, index) in movies" :key="index">
        <a :href="`https://www.themoviedb.org/movie/${movie.id}`">
          <img
            :src="`https://image.tmdb.org/t/p/w1280/${movie.backdrop_path}`"
            :alt="movie.title"
          />
        </a>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
import { Navigation, Pagination, Autoplay } from "swiper";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination, Autoplay],
    };
  },
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang="scss" scoped>
.movie__slider {
  margin-bottom: 50px;
  overflow: hidden;
  width: 100%;
  a {
    img {
      height: 450px;
      width: 100%;
      object-fit: cover;
    }
  }
}
</style>
