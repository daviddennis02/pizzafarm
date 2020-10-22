<template>
  <footer>
    <div class="container">
      <div>
        <img :src="LogoIcon" alt="logo" />
        <div class="contact">
          <div>Call Us</div>
          <div>123-405-20</div>
          <small>&copy; Copyright 2020</small>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Logo from '../../assets/images/logo.png'
export default {
  name: "Footer",
  data() {
    return {
        LogoIcon: Logo,
    };
  },
};
</script>

<style  scoped>
</style>