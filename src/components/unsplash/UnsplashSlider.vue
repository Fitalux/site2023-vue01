<template>
  <div class="unsplash__slider">
    <swiper
      :modules="modules"
      :slides-per-view="4"
      :spaceBetween="3"
      :pagination="{ clickable: true }"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 0 }"
      :speed="5000"
    >
      <swiper-slide v-for="(image, index) in images" :key="index">
        <a :href="`https://unsplash.com/photos/${image.id}`" target="_blank">
          <img :src="image.urls.regular" :alt="image.alt_description" />
        </a>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
// import Swiper from "swiper";
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
    images: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang="scss">
.unsplash__slider {
  overflow: hidden;
  width: 100%;
  margin-bottom: 50px;
  .swiper-wrapper {
    transition-timing-function: linear;
  }
  .swiper-slide {
    overflow: hidden;
    img {
      height: 350px;
      width: 100%;
      object-fit: cover;
      &:hover {
        scale: 1.3;
      }
      transition: all 0.6s;
    }
  }
}
</style>
