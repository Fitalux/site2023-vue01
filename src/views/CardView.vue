<template>
  <div>
    <ContTitle title="CARD" />
    <CardCont />
  </div>
</template>
<script>
import ContTitle from "@/components/layout/ConTitle.vue";
import CardCont from "@/components/card/CardCont.vue";

export default {
  components: {
    ContTitle,
    CardCont,
  },
};
</script>
