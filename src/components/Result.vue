<template>
  <div class="result">
    <div class="title">{{ results[getIndex].title }}</div>
    <div class="desc">{{ results[getIndex].desc }}</div>
  </div>
</template>

<script>
export default {
  name: "Result",
  props: ["results", "totalCorrect"],
  computed: {
    getIndex() {
      if (this.totalCorrect >= 3) return 1;

      return 0;
    },
  },
};
</script>
