<script setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue';
import Dropdown from './Dropdown.vue';

let open = ref(false);
let expand = ref(false);

const openMenu = () => {
  open.value = !open.value;
};

const expandSearch = () => {
  expand.value = !expand.value;
};
</script>

<template>
  <div
    class="flex items-center justify-between px-5 z-20 w-full lg:w-auto lg:justify-normal min-h-28 lg:gap-[20px] xl:gap-[50px]"
  >
    <div class="flex items-center gap-1 md:gap-3 xl:gap-8">
      <a href="/">
        <img src="../assets/logo.png" alt="logo" />
      </a>
      <nav class="">
        <ul
          class="gap-4 flex flex-col lg:flex-row lg:items-center absolute bg-white w-full lg:top-[110px] lg:h-[112px] left-0 pl-5 lg:pl-0 bg-red lg:static lg:flex lg:w-auto xl:gap-8 text-wrap duration-500 ease-in"
          :class="[open ? 'top-[110px] h-screen sm:h-auto' : 'top-[-120%]']"
        >
          <li
            class="items-baseline text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue lg:mt-0 mt-3 hover:bg-primaryLight p-1 rounded-md lg:p-0 lg:hover:bg-transparent"
          >
            <a href="#"> პოლიტიკა </a>
          </li>
          <li
            class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue lg:mt-0 mt-3 hover:bg-primaryLight p-1 rounded-md lg:p-0 lg:hover:bg-transparent"
          >
            <a href="#">საზოგადოება</a>
          </li>
          <li
            class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue lg:mt-0 mt-3 hover:bg-primaryLight p-1 rounded-md lg:p-0 lg:hover:bg-transparent"
          >
            <a href="#">სამართალი </a>
          </li>
          <li
            class="text-sm md:text-sm xl:text-base font-medium uppercase hidden lg:contents text-grey hover:cursor-pointer hover:text-blue hover:bg-primaryLight p-1 rounded-md lg:p-0 lg:hover:bg-transparent"
          >
            <a href="#"> ბიზნესი & ეკონომიკა </a>
          </li>
          <Dropdown v-if="!open" />
          <div v-if="open" class="flex flex-col gap-4">
            <li
              class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue hover:bg-primaryLight w-full p-1 rounded-md"
            >
              <a href="#"> ბიზნესი & ეკონომიკა </a>
            </li>
            <li
              class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue hover:bg-primaryLight w-full p-1 rounded-md"
            >
              <a href="#"> მსოფლიო </a>
            </li>
            <li
              class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue hover:bg-primaryLight w-full p-1 rounded-md"
            >
              <a href="#"> ხელოვნება </a>
            </li>
            <li
              class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue hover:bg-primaryLight w-full p-1 rounded-md"
            >
              <a href="#"> სპორტი </a>
            </li>
            <li
              class="text-sm md:text-sm xl:text-base font-medium uppercase text-grey hover:cursor-pointer hover:text-blue mb-10 hover:bg-primaryLight w-full p-1 rounded-md"
            >
              <a href="#">რელიგია </a>
            </li>
            <div
              class="md:hidden flex flex-row justify-center items-center gap-5 static mb-5"
            >
              <a href="#">
                <Icon
                  class="border-0 bg-lightBlue rounded-3xl p-2"
                  icon="mdi:instagram"
                  width="35"
                  color="#212121"
                />
              </a>
              <a href="#">
                <Icon
                  class="border-0 bg-lightBlue rounded-3xl p-2"
                  icon="mdi:facebook"
                  width="35"
                  color="#212121"
                />
              </a>
            </div>
          </div>
        </ul>
      </nav>
    </div>
    <div class="flex gap-4 items-center">
      <div class="md:flex md:items-center md:gap-2 md:static hidden">
        <a href="#">
          <Icon
            class="border-0 bg-lightBlue rounded-3xl p-2"
            icon="mdi:instagram"
            width="35"
            color="#212121"
          />
        </a>
        <a href="#">
          <Icon
            class="border-0 bg-lightBlue rounded-3xl p-2"
            icon="mdi:facebook"
            width="35"
            color="#212121"
          />
        </a>
      </div>

      <div class="relative">
        <input
          class="border-0 bg-lightBlue text-sm sm:text-base rounded-full md:w-30 lg:w-40 lg:h-[48px] 2xl:w-56 2xl:rounded-3xl p-3 focus:outline-blue focus:outline-1 sm:focus:outline-2 w-[35px] h-[35px] md:w-40"
          :class="[expand ? 'w-[170px]' : 'w-[35px] h-[35px]']"
          type="text"
          id="text"
          :placeholder="expand ? 'ძიება' : ''"
          v-model="text"
        />
        <Icon
          class="absolute lg:top-[13px] lg:right-2 top-[8px] right-1.5 lg:w-[25px] lg:h-[25px] w-[20px] h-[20px] hover:cursor-pointer"
          icon="mdi:magnify"
          @click="expandSearch()"
        />
      </div>

      <Icon
        v-if="!open"
        icon="mdi:menu"
        width="35"
        class="border-0 bg-lightBlue rounded-3xl p-2 lg:hidden hover:cursor-pointer"
        @click="openMenu"
      />
      <Icon
        v-if="open"
        icon="mdi:window-close"
        width="35"
        class="border-0 bg-lightBlue rounded-3xl p-2 lg:hidden hover:cursor-pointer"
        @click="openMenu"
      />
    </div>
  </div>
</template>
