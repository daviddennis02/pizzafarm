<template>
  <div>
    <carousel :per-page="1" :mouse-drag="true" :paginationEnabled="true"  :loop="false">
      <slide v-for="(slide, index) in slides" :key="index">
        <div class="slider_bck" :style="{ background: `url(${slide.bkg})` }">
          <div class="container slider-container">
            <div class="text">
              <div>{{ slide.text }}</div>
            </div>
            <div class="image">
              <img :src="slide.img" :alt="slide.alt" />
            </div>
          </div>
        </div>
      </slide>
    </carousel>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
import slideBkg1 from "../../assets/images/slide_bck.jpg";
import slideBkg2 from "../../assets/images/slide_bck.jpg";

import pizzaOne from "../../assets/images/pizza_one.png";
import pizzaTwo from "../../assets/images/pizza_three.png";

export default {
  name: "slider",
  components: {
    Carousel,
    Slide,
  },
  data() {
    return {
      slides: [
        {
          text: "20% OFF ON  ALL PIZZAS",
          bkg: slideBkg1,
          img: pizzaOne,
          alt: "background image",
        },
        {
          text: "BUY TWO, GET ONE FREE",
          bkg: slideBkg2,
          img: pizzaTwo,
          alt: "background image",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
