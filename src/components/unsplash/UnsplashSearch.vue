<template>
  <div class="unsplash__search">
    <h2 class="blind">검색하기</h2>
    <input
      ref="inputRef"
      type="search"
      @keypress="onKeyPress"
      placeholder="검색어를 입력하세요."
    />
    <button type="submit" @click="onClick">검색</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "UnsplashSearch",
  setup(props, { emit }) {
    const inputRef = ref(null);

    const handleSearch = () => {
      const value = inputRef.value.value;
      emit("onSearch", value);
    };

    const onKeyPress = (event) => {
      if (event.key === "Enter") {
        handleSearch();
      }
    };

    const onClick = () => {
      handleSearch();
    };

    return {
      inputRef,
      onKeyPress,
      onClick,
    };
  },
};
</script>

<style lang="scss">
.unsplash__search {
  margin-bottom: 50px;
  text-align: center;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include B-radius(15px);
    min-width: 300px;
    margin-right: 10px;
    font-family: "NanumSquareNeo";
    border: 1px solid #4857ec;
  }

  button {
    @include button(#4857ec, #fff);
    @include B-radius(15px);
    font-family: "NanumSquareNeo";
  }
}
</style>
