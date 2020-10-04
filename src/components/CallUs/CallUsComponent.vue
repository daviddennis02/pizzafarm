<template>
  <div class="call_us_container">
    <div class="container">
      <div class="first" v-scroll-reveal.reset="{ delay: 200, scale: 1 }">
        <h1>Hungry ?</h1>
      </div>

      <div
        class="second"
        v-scroll-reveal="{
          delay: 300,
          afterReveal: () => {
            secondAnim = true;
          },
        }"
      >
        <div v-if="secondAnim"><AnimationComponent /></div>
      </div>

      <div class="third" v-scroll-reveal.reset="{ delay: 600, scale: 1 }">
        <span>Give Us a Call </span><span> 666-88880</span>
      </div>
    </div>
  </div>
</template>

<script>
import AnimationComponent from "./AnimationComponent.vue";
export default {
  name: "CallUs",
  components: {
    AnimationComponent,
  },
  data(){
      return{
          secondAnim: false,
      }
  }
};
</script>

<style scoped></style>
