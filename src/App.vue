<script setup>
import Header from './components/Header.vue';
import MainSlide from './components/MainSlide.vue';
import SmallSlide from './components/SmallSlide.vue';
import GridSection from './components/GridSection.vue';
import NewsList from './components/NewsList.vue';
import PopularList from './components/PopularList.vue';
</script>

<template>
  <div class="bg-background h-full">
    <div class="flex lg:justify-center items-center bg-white">
      <Header />
    </div>
    <div class="flex xl:flex-row flex-col gap-[14px] justify-center mt-10">
      <div
        class="flex-col px-[10px] md:px-50px xl:p-0 lg:justify-center items-center w-full xl:w-[976px]"
      >
        <MainSlide />
        <div class="flex flex-col sm:flex-row gap-[32px] lg:hidden static my-5">
          <NewsList />
          <PopularList />
        </div>
        <SmallSlide />
        <GridSection />
      </div>
      <div class="lg:flex lg:flex-col lg:gap-[66px] lg:static hidden">
        <NewsList />
        <PopularList />
      </div>
    </div>
  </div>
</template>
