<template>
  <div className="youtube__cont container">
    <ul>
      <li v-for="(youtube, index) in youtubes" :key="index">
        <a
          :href="`https://www.youtube.com/watch?v=${youtube.id.videoId}`"
          target="_blank"
        >
          <img
            :src="youtube.snippet.thumbnails.medium.url"
            :alt="youtube.snippet.title"
          />
          <span>{{ youtube.snippet.title }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    font-family: "NanumSquareNeo";

    li {
      width: 24%;
      position: relative;
      margin-bottom: 2%;
    }
  }
}
</style>
