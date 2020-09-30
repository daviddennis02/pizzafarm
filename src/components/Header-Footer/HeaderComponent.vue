<template>
  <header>
    <div class="container clear">
      <div class="logo">logo</div>
      <div class="nav">nav</div>
    </div>
  </header>
</template>

<script>
import Logo from '../../assets/images/logo.png';
import Menu from '../../assets/images/menu.png';

export default {
    name: 'HeaderComponent',
    components:{},
    data(){
        return{
            LogoIcon: Logo,
            MenuIcon: Menu
        }
    }
};
</script>

<style  scoped>

</style>