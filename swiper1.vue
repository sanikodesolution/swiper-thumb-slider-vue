<template>
  <section class="testimonial-section-home5 position-relative">
    <div class="bg" style="background-image: url(./images/background/1.jpg)"></div>
    <div class="auto-container">
      <div class="testimonials">
        <div class="swiper-container testimonial-content-home5">
          <!-- Main Swiper -> pass thumbs swiper instance -->
          <swiper
            :style="{
              '--swiper-navigation-color': '#fff',
                '--swiper-pagination-color': '#fff',
              }"
              :spaceBetween="10"
              :navigation="false"
              :loop="true"
              :pagination="{ clickable: true,}"
              :thumbs="{ swiper: thumbsSwiper }"
              :modules="modules"
              class="mySwiper2">
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-1.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-2.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-3.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-4.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-5.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-6.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-7.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-8.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-9.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-10.jpg" /></swiper-slide>
            </swiper>
            <swiper
              @swiper="setThumbsSwiper"
              :spaceBetween="10"
              :slidesPerView="4"
              :freeMode="true"
              :watchSlidesProgress="true"
              :modules="modules"
              class="mySwiper">
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-1.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-2.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-3.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-4.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-5.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-6.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-7.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-8.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-9.jpg" /></swiper-slide>
              <swiper-slide><img src="https://swiperjs.com/demos/images/nature-10.jpg" /></swiper-slide>
            </swiper>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import { ref } from 'vue';
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/free-mode';
import 'swiper/css/navigation';
import 'swiper/css/thumbs';


// import required modules
import { FreeMode, Navigation, Pagination, Thumbs } from 'swiper/modules';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const thumbsSwiper = ref(null);
      const setThumbsSwiper = (swiper) => {
        thumbsSwiper.value = swiper;
      };
      return {
        Thumbs,
        thumbsSwiper,
        setThumbsSwiper,
        modules: [FreeMode, Navigation, Pagination, Thumbs],
      };
    },
  };
</script>
