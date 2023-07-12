<template>
  <div class="youtube__tag">
    <div>
      <button @click="onClick('AJR')">AJR</button>
      <button @click="onClick('Taylor Swift')">Taylor Swift</button>
      <button @click="onClick('Imagine Dragons')">Imagine Dragons</button>
      <button @click="onClick('NF')">NF</button>
      <button @click="onClick('Coldplay')">Coldplay</button>
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
.youtube__tag {
  // display: none
  div {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 50px;

    button {
      background-color: #fff;
      border: 1px solid #00c183;
      padding: 10px 20px;
      margin: 0 10px;
      color: #00c183;
      cursor: pointer;
      font-family: "NanumSquareNeo";
      transition: all 0.5s;

      &:hover {
        background-color: #00c183;
        color: #fff;
      }
    }
  }
}
</style>
