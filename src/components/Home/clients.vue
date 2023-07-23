<template>
  <div style="position: relative">
    <div class="wraper text-center">
      <h2 style="color: #9753a0">من عملائنا المميزين</h2>
      <div class="my-5">
        <swiper
          :breakpoints="swiperOptions.breakpoints"
          :modules="modules"
          navigation
          :pagination="{ clickable: true }"
        >
          <swiper-slide
            ><div class="">
              <img src="@/assets/images/home/client1.png" alt="" /></div
          ></swiper-slide>
        </swiper>
      </div>
      <router-link :to="{ name: 'allClients' }">
        <Button text="المزيد" />
      </router-link>
    </div>
  </div>
</template>

<script>
import Button from "@/components/button.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, EffectFade } from "swiper";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
import "swiper/css";
export default {
  name: "clients",
  components: {
    Button,
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Navigation, EffectFade],
      swiperOptions: {
        breakpoints: {
          500: {
            slidesPerView: 1,
            slidesToScroll:1,
          },

          700: {
            slidesPerView: 2,
            slidesToScroll:2,
            spaceBetween: 60,
          },
          900: {
            slidesPerView: 3,
            slidesToScroll:3,
            spaceBetween: 60,
          },

          1025: {
            slidesPerView: 4,
            slidesToScroll:4,
            spaceBetween: 60,
          },
        },
      },
    };
  },
};
</script>

<style scoped></style>
