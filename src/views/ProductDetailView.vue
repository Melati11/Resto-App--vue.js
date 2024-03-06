<template>
  <div>
    <DetailMobile v-if="isMobile" />
    <DetailDesktop v-else />
  </div>
</template>

<style scoped>
</style>

<script>
import DetailDesktop from "@/components/ProductDetailPage/Desktop/ProductDetailPage.vue";
import DetailMobile from "@/components/ProductDetailPage/Mobile/ProductDetailPage.vue";
export default {
  name: "DetailPage",
  components: {
    DetailDesktop,
    DetailMobile,
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
