<template>
  <section id="sliderSection" :class="attr">
    <h2 class="blind">이미지 슬라이드</h2>
    <div class="slider__inner">
      <div class="slider__img">
        <swiper
          :modules="modules"
          :slides-per-view="1"
          :space-between="50"
          navigation
          :pagination="{ clickable: true }"
          :scrollbar="{ draggable: true }"
          :autoplay="{
            delay: 2500,
            disableOnInteraction: false,
          }"
          @swiper="onSwiper"
          @slideChange="onSlideChange"
        >
          <swiper-slide v-for="(slider, index) in sliders" :key="index">
            <div class="slider s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p>{{ slider.desc }}</p>
                <a href="/" class="more button-black">더 보 기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage1" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </swiper-slide>
          <!-- slider01 -->

          <swiper-slide>
            <div class="slider s2 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p>{{ slider.desc }}</p>
                <a href="/" class="more button-black"> 더 보 기 </a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage1" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </swiper-slide>
          <!-- slider02 -->

          <swiper-slide>
            <div class="slider s3 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p>{{ slider.desc }}</p>
                <a href="/" class="more button-black">더 보 기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage1" :alt="slider.title" />
                <img :src="slider.iconImage1" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </swiper-slide>
          <!-- slider03 -->
        </swiper>
      </div>
    </div>
  </section>
</template>

<script>
// import Swiper core and required modules
import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

export default {
  props: {
    attr: String,
  },
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
      modules: [Navigation, Pagination, Scrollbar, A11y, Autoplay],
    };
  },
  data: function () {
    return {
      sliders: [
        {
          title: "MUSIC<br />Recommend",
          desc: "요즘 들을 거 없나? 싶을 때 취향을 강타할 MUSIC",
          iconImage1: "./images/slider/sliderIcon02.png",
          iconImage2: "./images/slider/sliderIcon03.png",
          iconImage3: "./images/slider/sliderIcon04.png",
        },
        {
          title: "MUSIC<br />Recommend",
          desc: "요즘 들을 거 없나? 싶을 때 취향을 강타할 MUSIC",
          iconImage1: "./images/slider/sliderIcon02.png",
          iconImage2: "./images/slider/sliderIcon03.png",
          iconImage3: "./images/slider/sliderIcon04.png",
        },
        {
          title: "MUSIC<br />Recommend",
          desc: "요즘 들을 거 없나? 싶을 때 취향을 강타할 MUSIC",
          iconImage1: "./images/slider/sliderIcon02.png",
          iconImage2: "./images/slider/sliderIcon03.png",
          iconImage3: "./images/slider/sliderIcon04.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.slider__wrap {
  background-color: rgba(146, 230, 243, 0.2);
}

.slider__inner {
  position: relative;
  .slider__img {
    .slider {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 800;
          text-transform: uppercase;
          line-height: 1;
          padding-top: 100px;
          margin-bottom: 40px;
        }
        p {
          font-size: 24px;
          line-height: 1.3;
          margin-bottom: 50px;
        }
        .more {
          font-size: 18px;
        }
      }

      .img {
        position: absolute;
        right: 0;
        top: -50px;
        width: 600px;
        height: 600px;
        background-image: url(@/assets/images/slider/sliderIcon01.jpg);
        background-size: cover;
        background-position: center;

        img {
          &:nth-child(1) {
            position: absolute;
            width: 300px;
            left: -30px;
            transform: rotate(-25deg);
          }
          &:nth-child(2) {
            position: absolute;
            width: 300px;
            right: 0;
            bottom: 140px;
          }
          &:nth-child(3) {
            position: absolute;
            width: 250px;
            bottom: 50px;
            left: 30px;
          }
        }
      }

      .circle {
        span {
          display: block;
          position: absolute;
          left: 50%;
          top: 50%;
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }
        span:nth-child(1) {
          background-color: var(--button_bule);
          left: 10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_green);
          top: 20%;
          left: -10%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_red);
          left: 100%;
          top: 10%;
        }
        span:nth-child(4) {
          background-color: var(--button_green);
          left: 17%;
          top: -10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(5) {
          background-color: var(--button_bule);
          left: 90%;
          top: 80%;
          width: 30px;
          height: 30px;
        }
      }
    }
  }

  .slider__btn {
    > a {
      position: absolute;
      width: 25px;
      height: 40px;
      top: 50%;
      background-repeat: no-repeat;
      background-position: center;
      transform: translateY(-50%);
    }
    .left {
      left: 30px;
      background-image: url(@/assets/images/slider/slider__left.png);
    }

    .right {
      right: 30px;
      background-image: url(@/assets/images/slider/slider__right.png);
    }
  }

  .slider__dot {
    position: absolute;
    left: 50%;
    bottom: -70px;
    transform: translateX(-50%);

    a {
      display: inline-block;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      margin: 0 5px;
      border: 5px solid transparent;
      background-color: #4857ec;
      box-shadow: 0 0 0 5px #4857ec transparent;
      transition: all 0.5s;
      &.active {
        box-shadow: 0 0 0 5px #4857ec;
        border-width: 4px;
        background-color: #fff;
      }
      &:hover {
        transform: scale(1.2);
      }
    }
  }
}
</style>
