<template>
  <div v-if="inputData" class="header">
    <img class="header--img" :src="logo" alt="logo" />
    <div class="header--item" v-for="(value, key) in inputData" :key="key">
      <a
        class="header--link"
        v-text="value.name"
        @click="toggleNavigationItem(value.id)"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    inputData: {
      type: Array,
      default: () => {
        return [
          {
            id: "#page",
            name: "Home",
          },
        ];
      },
    },
  },
  name: "AppHeader",
  data() {
    return {
      logo: "https://cdn.mainlycoding.com/xQLq9YtnepVOVkWyQaC2.jpg",
    };
  },
  methods: {
    toggleNavigationItem(scroll) {
      this.$emit("clickedNavigation", scroll);
    },
  },
};
</script>
