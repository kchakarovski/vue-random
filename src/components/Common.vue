<template>
  <div class="common" :id="navData.id"></div>
</template>

<script>
export default {
  name: "common",
  data() {
    return {};
  },
  props: {
    navData: {
      type: Object,
      default: () => {
        return {
          id: "#home-section"
        };
      }
    }
  }
};
</script>

<style></style>
