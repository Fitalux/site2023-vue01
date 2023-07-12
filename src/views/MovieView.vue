<template>
  <ConTitle title="movie" />
  <MovieSearch @onSearch="search" />
  <MovieTag @onSearch="search" />
  <MovieCont :movies="movies" />
</template>

<script>
import ConTitle from "@/components/layout/ConTitle.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
// import { ref } from "vue";

export default {
  name: "MovieView",
  components: {
    ConTitle,
    MovieSearch,
    MovieTag,
    MovieCont,
  },
  data() {
    return {
      movies: [],
    };
  },
  methods: {
    async tags(query) {
      try {
        const response = await fetch(
          `${query}?api_key=697729d3f274ce88cf5729d38280fd33`
        );
        const result = await response.json();
        this.movies = result.results;
      } catch (error) {
        console.log(error);
      }
    },
    async search(query) {
      try {
        const response = await fetch(
          `https://api.themoviedb.org/3/search/movie?api_key=ec712643f661ae9c053a7a5c3ab5855d&query=${query}`
        );

        const result = await response.json();
        this.movies = result.results;
      } catch (error) {
        console.log("error", error);
      }
    },
  },
  async created() {
    try {
      const response = await fetch(
        "https://api.themoviedb.org/3/movie/popular?api_key=ec712643f661ae9c053a7a5c3ab5855d"
      );
      const result = await response.json();
      this.movies = result.results;
    } catch (error) {
      console.log("error", error);
    }
  },
};
</script>
