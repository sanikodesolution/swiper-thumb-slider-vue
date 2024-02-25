<template>
  <section class="testimonial-section-home5 position-relative">
    <div class="bg" style="background-image: url(./images/background/1.jpg)"></div>
    <div class="auto-container">
      <div class="testimonials">
        <div class="swiper-container testimonial-content-home5">
          <!-- Main Swiper -> pass thumbs swiper instance -->
          <swiper :modules="[Thumbs]" :thumbs="{ swiper: thumbsSwiper }"
            :slides-per-view="1"
            :space-between="30"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
          >
            <swiper-slide class="testimonial-block-home5">
              <div class="inner-box">
                <div class="image-box"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-1.png" alt=""></figure></div>
                <div class="text">This is due to their excellent service, competitive pricing and customer support. It’s throughly refresing to get such a personal touch.</div>
                <h4 class="name">Christine Eve</h4>
              </div>
            </swiper-slide>
            <swiper-slide class="testimonial-block-home5">
              <div class="inner-box">
                <div class="image-box"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-1.png" alt=""></figure></div>
                <div class="text">competitive pricing and customer support. It’s throughly refresing to get such a personal touch. This is due to their excellent service, </div>
                <h4 class="name">Christine Eve</h4>
              </div>
            </swiper-slide>
            <swiper-slide class="testimonial-block-home5">
              <div class="inner-box">
                <div class="image-box"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-1.png" alt=""></figure></div>
                <div class="text">pricing and customer support. It’s throughly refresing to get such This is due to their excellent service, competitive a personal touch.</div>
                <h4 class="name">Christine Eve</h4>
              </div>
            </swiper-slide>
            <swiper-slide class="testimonial-block-home5">
              <div class="inner-box">
                <div class="image-box"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-1.png" alt=""></figure></div>
                <div class="text">pricing and customer support. It’s throughly refresing to get such This is due to their excellent service, competitive a personal touch.</div>
                <h4 class="name">Christine Eve</h4>
              </div>
            </swiper-slide>
          </swiper>
        </div>

        <!-- It is also required to set watchSlidesProgress prop -->
        <div class="swiper-container testimonial-thumbs-home5">
          <div class="swiper-wrapper">
            <swiper
              :slides-per-view="3"
              :modules="[Thumbs]"
              watch-slides-progress
              @swiper="setThumbsSwiper"
              :space-between="10"
            >
              <swiper-slide class="testimonial-thumb"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-1.jpg" alt=""></figure></swiper-slide>
              <swiper-slide class="testimonial-thumb"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-2.jpg" alt=""></figure></swiper-slide>
              <swiper-slide class="testimonial-thumb"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-1.jpg" alt=""></figure></swiper-slide>
              <swiper-slide class="testimonial-thumb"><figure class="image"><img class="rounded-circle" src="/images/resource/testi-2.jpg" alt=""></figure></swiper-slide>
            </swiper>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
  import { ref } from 'vue';
  import { Thumbs } from 'swiper/modules';
  import { Swiper, SwiperSlide } from 'swiper/vue';

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
      };
    },
  };
</script>