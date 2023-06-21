<template>
  <div>
    <main>
      <SliderSection attr="slider__wrap Neo5 section" />
      <IntroSection attr="intro__wrap section bg-blue Neo5" />
      <ImageSection attr="images__wrap section center Neo5" />
      <YoutubeSection attr="youtube__wrap section Neo5" />
      <UnsplashSection attr="unsplash__wrap section Neo5" />
      <MovieSection attr="movie__wrap section Neo5" />
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import ImageSection from "@/components/section/ImageSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";

export default {
  components: {
    SliderSection,
    IntroSection,
    ImageSection,
    YoutubeSection,
    UnsplashSection,
    MovieSection,
  },
};
</script>
