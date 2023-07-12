<template>
  <ConTitle title="unsplash" />
  <UnsplashSearch @onSearch="search" />
  <UnsplashTag @onSearch="search" />
  <UnsplashCont :images="images" />
</template>

<script>
import ConTitle from "@/components/layout/ConTitle.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { onMounted, ref } from "vue";

export default {
  components: {
    ConTitle,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },

  setup() {
    const images = ref([]);

    const search = async (query) => {
      try {
        const response = await fetch(
          `https://api.unsplash.com/search/photos?client_id=I7ba-CzsJwZ63mWvfrS0T7KpHn56pL6ett68uoeQtIw&per_page=30&query=${query}`
        );
        const result = await response.json();
        images.value = result.results;
      } catch (error) {
        console.log("error", error);
      }
    };

    onMounted(async () => {
      try {
        const response = await fetch(
          "https://api.unsplash.com/photos?client_id=I7ba-CzsJwZ63mWvfrS0T7KpHn56pL6ett68uoeQtIw&"
        );
        const result = await response.json();
        images.value = result;
      } catch (error) {
        console.log("error", error);
      }
    });

    return {
      images,
      search,
    };
  },
};
</script>
