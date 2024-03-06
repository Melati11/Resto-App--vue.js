<template>
  <div id="app">
    <router-view />
    <footer-view></footer-view>
  </div>
</template>

<script>
import FooterView from "./components/Footer.vue";
export default {
  components: { FooterView },
};
</script>
