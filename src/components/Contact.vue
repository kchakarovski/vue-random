<template>
  <div class="contact" :id="inputData.id"></div>
</template>

<script>
export default {
  name: "contact",
  data() {
    return {};
  },
  props: {
    inputData: {
      type: Object,
      default: () => {
        return {
          id: "#contact-section"
        };
      }
    }
  }
};
</script>

<style></style>
