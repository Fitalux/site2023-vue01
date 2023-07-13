<template>
  <div>
    <ContTitle title="INTRO" />
    <IntroCont />
  </div>
</template>
<script>
import ContTitle from "@/components/layout/ConTitle.vue";
import IntroCont from "@/components/intro/IntroCont.vue";

export default {
  components: {
    ContTitle,
    IntroCont,
  },
};
</script>
