<script>
import { Swiper, SwiperSlide, useSwiper } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';

// import './style.css';

// import required modules
import { Pagination, Navigation } from 'swiper/modules';
const slideData = [
  {
    id: 1,
    src: 'src/assets/images/slideimage.jpeg',
    date: '12.08.2023',
    tag: 'პოლიტიკა',
    title:
      'ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების ინფრასტრუქტურული პროექტები დაიწყება',
    about:
      ' განთავსების (ლისტინგის) ორგანიზატორი სომხეთის ბანკი სს “არდშიბანკია”. ობლიგაციის ნომინალი - 1000 USD',
  },
  {
    id: 2,
    src: 'src/assets/images/slideimage.jpeg',
    date: '12.08.2023',
    tag: 'პოლიტიკა',
    title:
      'ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების ინფრასტრუქტურული პროექტები დაიწყება',
    about:
      ' განთავსების (ლისტინგის) ორგანიზატორი სომხეთის ბანკი სს “არდშიბანკია”. ობლიგაციის ნომინალი - 1000 USD',
  },
  {
    id: 3,
    src: 'src/assets/images/slideimage.jpeg',
    date: '12.08.2023',
    tag: 'პოლიტიკა',
    title:
      'ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების ინფრასტრუქტურული პროექტები დაიწყება',
    about:
      ' განთავსების (ლისტინგის) ორგანიზატორი სომხეთის ბანკი სს “არდშიბანკია”. ობლიგაციის ნომინალი - 1000 USD',
  },
  {
    id: 4,
    src: 'src/assets/images/slideimage.jpeg',
    date: '12.08.2023',
    tag: 'პოლიტიკა',
    title:
      'ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების ინფრასტრუქტურული პროექტები დაიწყება',
    about:
      ' განთავსების (ლისტინგის) ორგანიზატორი სომხეთის ბანკი სს “არდშიბანკია”. ობლიგაციის ნომინალი - 1000 USD',
  },
];
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
      slideData,
    };
  },
};
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
      class="mySwiper flex w-full sm:h-[406px] rounded-2xl"
      id="swiper"
    >
      <swiper-slide v-for="data in slideData" :key="data.id"
        ><img
          class="block object-cover sm:w-full sm:h-full"
          :src="data.src"
          alt="mountains"
      /></swiper-slide>
    </swiper>
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
      <p id="test">dasda</p>
    </div>
  </div>
</template>

<style scoped>
#swiper.swiper-button-prev,
.swiper-button-next {
  background-color: #fff !important;
  border-radius: 50%;
  color: #212121 !important;
}
</style>
