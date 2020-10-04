<template>
  <div>
    <HeaderComponent />
    <div>
      <SliderComponent />
      <MenuComponent />
      <CallUsComponent />
      <Newsletter />
    </div>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/Header-Footer/HeaderComponent.vue";
import FooterComponent from "./components/Header-Footer/FooterComponent.vue";
import SliderComponent from "./components/Featured/SliderComponent.vue";
import MenuComponent from "./components/Menu/MenuComponent.vue";
import CallUsComponent from "./components/CallUs/CallUsComponent.vue";
import Newsletter from "./components/Newsletter/NewsletterComponent.vue";
export default {
  name: "App",
  components: {
    HeaderComponent,
    FooterComponent,
    SliderComponent,
    MenuComponent,
    CallUsComponent,
    Newsletter,
  },
  data() {
    return {};
  },
};
</script>

<style>
@import "./assets/style.css";
</style>
