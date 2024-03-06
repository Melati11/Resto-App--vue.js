<template>
  <div>
    <ProductDetailDesktop v-if="isMobile" />
    <ProductDetailMobile v-else />
  </div>
</template>

<style scoped></style>

<script>
import ProductDetailDesktop from "@/components/ProductDetailPage/Mobile/ProductDetailPage.vue";
import ProductDetailMobile from "@/components/ProductDetailPage/Desktop/ProductDetailPage.vue";
export default {
  name: "homepage",
  components: {
    ProductDetailDesktop,
    ProductDetailMobile,
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
