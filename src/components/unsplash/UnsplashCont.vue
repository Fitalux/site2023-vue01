<template>
  <div className="unsplash__cont container">
    <ul>
      <li v-for="(image, index) in images" :key="index">
        <a :href="`https://unsplash.com/photos/${image.id}`" target="_blank">
          <img :src="image.urls.regular" :alt="image.alt_description" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
//unsplash Page
.unsplash__cont {
  ul {
    column-count: 4;

    li {
      margin-bottom: 20px;
    }
  }
}
</style>
