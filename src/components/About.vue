<template>
  <div class="about" :id="inputData.id"></div>
</template>

<script>
export default {
  name: "about",
  data() {
    return {};
  },
  props: {
    inputData: {
      type: Object,
      default: () => {
        return{
          id: "#about-section",
        }
      }
    },
  },
};
</script>

<style></style>
