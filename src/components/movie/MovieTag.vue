<template>
  <div class="movie__tag">
    <div>
      <button @click="onClick('Comic')">Comic</button>
      <button @click="onClick('Horror')">Horror</button>
      <button @click="onClick('Musical')">Musical</button>
      <button @click="onClick('Action')">Action</button>
      <button @click="onClick('Fantasy')">Fantasy</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    onClick(value) {
      this.$emit("onSearch", value);
    },
  },
};
</script>
<style lang="scss">
.movie__tag {
  // display: none
  div {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;

    button {
      background-color: #fff;
      border: 1px solid #101010;
      padding: 10px 20px;
      margin: 0 10px;
      color: #101010;
      cursor: pointer;
      font-family: "NanumSquareNeo";

      transition: all 0.5s;

      &:hover {
        background-color: #101010;
        color: #fff;
      }
    }
  }
}
</style>
