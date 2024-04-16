<script>
import { Swiper, SwiperSlide, useSwiper } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';

// import './style.css';

// import required modules
import { Pagination, Navigation } from 'swiper/modules';
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
    };
  },
};
const swiper = useSwiper();
</script>

<template>
  <div class="border-lg p-5 bg-white rounded-2xl lg:w-auto xl:max-w-[976px]">
    <swiper
      :slidesPerView="1"
      :spaceBetween="30"
      :loop="true"
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :modules="modules"
      class="mySwiper flex w-full h-[406px] rounded-2xl"
    >
      <swiper-slide
        ><img
          class="block object-cover w-full h-full"
          src="../assets/images/slideimage.jpeg"
          alt="mountains"
      /></swiper-slide>
      <swiper-slide
        ><img
          class="block object-cover w-full h-full"
          src="../assets/images/slideimage.jpeg"
          alt="mountains"
      /></swiper-slide>
    </swiper>
    <!-- <p @click="next">next</p> -->
    <div class="flex-col gap-2 mt-4">
      <div class="flex gap-3">
        <p
          class="bg-background px-2 py-1 rounded-3xl text-bold text-xs flex items-center justify-center"
        >
          12.08.2023
        </p>
        <p
          class="bg-background px-2 rounded-3xl text-bold text-xs flex items-center justify-center"
        >
          პოლიტიკა
        </p>
      </div>
      <h2 class="text-2xl">
        ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების ინფრასტრუქტურული
        პროექტები დაიწყება
      </h2>
      <p class="text-lg text-grey">
        განთავსების (ლისტინგის) ორგანიზატორი სომხეთის ბანკი სს “არდშიბანკია”.
        ობლიგაციის ნომინალი - 1000 USD
      </p>
    </div>
  </div>
</template>

<style scoped>
.swiper-button-prev {
  background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%2027%2044'%3E%3Cpath%20d%3D'M0%2C22L22%2C0l2.1%2C2.1L4.2%2C22l19.9%2C19.9L22%2C44L0%2C22L0%2C22L0%2C22z'%20fill%3D'%234c71ae'%2F%3E%3C%2Fsvg%3E") !important;
}

.swiper-button-next {
  background-image: url('../assets/images/arrowL.png') !important;
  background-image: url();
}
</style>
