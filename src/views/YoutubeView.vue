<template>
  <ConTitle title="youtube" />
  <YoutubeSearch @onSearch="search" />
  <YoutubeTag @onSearch="search" />
  <YoutubeCont :youtubes="youtubes" />
</template>

<script>
import ConTitle from "@/components/layout/ConTitle.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { onMounted, ref } from "vue";

export default {
  components: {
    ConTitle,
    YoutubeSearch,
    YoutubeTag,
    YoutubeCont,
  },

  setup() {
    const youtubes = ref([]);

    const search = async (query) => {
      try {
        const response = await fetch(
          `https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=28&q=${query}&type=video&key=AIzaSyCqJS_h2cF5AWsJiFlnsxH90Mbm-vlZzxw`
        );
        const result = await response.json();
        youtubes.value = result.items;
      } catch (error) {
        console.log("error", error);
      }
    };

    onMounted(async () => {
      try {
        const response = await fetch(
          "https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=28&q=coldplay&type=video&key=AIzaSyCqJS_h2cF5AWsJiFlnsxH90Mbm-vlZzxw"
        );
        const result = await response.json();
        youtubes.value = result.items;
      } catch (error) {
        console.log("error", error);
      }
    });

    return {
      youtubes,
      search,
    };
  },
};
</script>
