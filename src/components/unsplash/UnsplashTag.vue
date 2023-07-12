<template>
  <div class="unsplash__tag">
    <div>
      <button @click="onClick('Moon')">Moon</button>
      <button @click="onClick('Star')">Star</button>
      <button @click="onClick('Milky Way')">Milky Way</button>
      <button @click="onClick('Ocen')">Ocen</button>
      <button @click="onClick('Sunset')">Sunset</button>
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
.unsplash__tag {
  // display: none
  div {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;

    button {
      background-color: #fff;
      border: 1px solid #4857ec;
      padding: 10px 20px;
      margin: 0 10px;
      color: #4857ec;
      cursor: pointer;
      font-family: "NanumSquareNeo";
      transition: all 0.5s;

      &:hover {
        background-color: #4857ec;
        color: #fff;
      }
    }
  }
}
</style>
