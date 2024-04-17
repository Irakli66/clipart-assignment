<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
import { ref } from 'vue';
import { Icon } from '@iconify/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';

// import required modules
import { Navigation } from 'swiper/modules';
const slideData = [
  {
    id: 1,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
  {
    id: 2,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
  {
    id: 3,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
  {
    id: 4,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
  {
    id: 5,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
  {
    id: 6,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
  {
    id: 7,
    src: 'src/assets/images/pic.png',
    about: ' ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების',
  },
];

export default {
  methods: {
    Navigation() {
      return Navigation;
    },
  },
  components: {
    Swiper,
    SwiperSlide,
    Icon,
  },
  setup() {
    const swiperInstance = ref();

    function onSwiper(swiper) {
      swiperInstance.value = swiper;
    }
    const swiperNextSlide = () => {
      swiperInstance.value.slideNext();
    };
    const swiperPrevSlide = () => {
      swiperInstance.value.slidePrev();
    };
    return {
      modules: [Navigation],
      slideData,
      swiperPrevSlide,
      swiperNextSlide,
      onSwiper,
    };
  },
};
</script>

<template>
  <div
    class="border-lg p-5 bg-white rounded-2xl lg:w-auto xl:max-w-[976px] gap-5 mt-[66px]"
  >
    <div class="flex justify-between items-center">
      <h2>ცნობილი ფაქტები</h2>
      <div class="flex gap-5">
        <Icon
          class="bg-white shadow-md p-2 rounded-full items-center flex justify-center hover:cursor-pointer"
          icon="ic:baseline-arrow-back-ios-new"
          width="35"
          @click="swiperPrevSlide"
        />
        <Icon
          class="bg-white shadow-md p-2 rounded-full items-center flex justify-center hover:cursor-pointer"
          icon="ic:baseline-arrow-forward-ios"
          width="35"
          @click="swiperNextSlide"
        />
      </div>
    </div>
    <swiper
      :slidesPerView="1"
      :spaceBetween="10"
      @swiper="onSwiper"
      :breakpoints="{
        '640': {
          slidesPerView: 1,
          spaceBetween: 20,
        },
        '768': {
          slidesPerView: 2,
          spaceBetween: 40,
        },
        '1024': {
          slidesPerView: 3,
          spaceBetween: 50,
        },
      }"
      :modules="modules"
      v-if="slideData"
      class="mySwiper mt-5 flex w-full rounded-2xl"
    >
      <swiper-slide v-for="data in slideData" :key="data.id">
        <div class="bg-background w-full p-3 rounded-2xl">
          <img
            class="block object-cover w-full h-full"
            v-bind:src="data?.src"
          />
          <p class="text-base">
            {{ data?.about }}
          </p>
        </div>
      </swiper-slide>
    </swiper>
    <!-- <img v-bind:src="imageObject.src" v-bind:alt="imageObject.alt" /> -->
  </div>
</template>
