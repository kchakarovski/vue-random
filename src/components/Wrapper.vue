<template>
  <div class="wrapper">
    <common />
    <about />
    <contact />
  </div>
</template>

<script>
import common from "./Common";
import about from "./About";
import contact from "./Contact";
export default {
  name: "wrapper",
  components: {
    common,
    about,
    contact
  },
  data() {
    return {};
  }
};
</script>

<style></style>
