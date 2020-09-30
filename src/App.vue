<template>
  <div>
    <HeaderComponent />
    <div>Content</div>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/Header-Footer/HeaderComponent.vue";
import FooterComponent from "./components/Header-Footer/FooterComponent.vue";
export default {
  name: "App",
  components: { HeaderComponent, FooterComponent },
  data() {
    return {};
  },
};
</script>

<style>
@import "./assets/style.css";
</style>