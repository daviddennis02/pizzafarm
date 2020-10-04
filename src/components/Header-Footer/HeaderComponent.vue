<template>
  <header>
    <div class="container clear">
      <div class="logo">
        <img :src="LogoIcon" alt="logo" />
      </div>
      <div class="nav">
        <img
          :src="MenuIcon"
          alt="menu"
          @click="showSidePanel = !showSidePanel"
        />
      </div>
      <md-drawer class="side-drawer" :md-active.sync="showSidePanel" :md-right="true" />
    </div>  
  </header> 
</template>

<script>
import Logo from "../../assets/images/logo.png";
import Menu from "../../assets/images/menu.png";

export default {
  name: "HeaderComponent",
  components: {},
  data() {
    return {
      LogoIcon: Logo,
      MenuIcon: Menu,
      showSidePanel: false,
    };
  },
};
</script>

<style scoped></style>
