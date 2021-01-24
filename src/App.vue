<template>
  <div id="app">
    <app-header
      :inputData="navigationInputData"
      @clickedNavigation="clickedNavigation"
    />
    <router-view />
    <app-footer />
  </div>
</template>
<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import { navigation } from "./static/navigation";
import { homeData } from "./static/pages";
import { mapGetters, mapActions } from "vuex";
export default {
  name: "app",
  components: {
    AppHeader,
    AppFooter,
  },
  data() {
    return {};
  },
  mounted() {
    this.getData();
  },
  computed: {
    ...mapGetters(["navigationInputData"]),
  },
  methods: {
    ...mapActions(["updateNavigationData", "updateHomeData"]),
    getData() {
      this.updateNavigationData(navigation);
      this.updateHomeData(homeData);
    },
    clickedNavigation(scroll) {
      document.getElementById(scroll).scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>
<style lang="scss"></style>
