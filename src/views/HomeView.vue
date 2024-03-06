<template>
  <div>
    <HomepageMobile v-if="isMobile" />
    <HomepageDesktop v-else />
  </div>
</template>

<style scoped>
</style>

<script>
import HomepageMobile from "@/components/Homepage/Mobile/Homepage.vue";
import HomepageDesktop from "@/components/Homepage/Desktop/Homepage.vue";
export default {
  name: "homepage",
  components: {
    HomepageDesktop,
    HomepageMobile,
  },
  data() {
    return {
      isMobile: false,
    };
  },
  methods: {
    handleView() {
      this.isMobile = screen.width <= 900;
    },
  },
  beforeMount() {
    this.handleView();
  },
};
</script>
