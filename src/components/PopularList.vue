<script setup>
import { Icon } from '@iconify/vue';

const popularListData = [
  {
    id: 1,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 2,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 3,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 4,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 5,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 6,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 7,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 8,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 9,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 10,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 11,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 12,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 13,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 14,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 15,
    src: '/src/assets/images/photo.png',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
];
</script>

<template>
  <div class="h-[330px] lg:h-[606px] p-3 2xl:w-[300px] bg-white rounded-2xl">
    <h3 class="font-bold text-xl">პოპულარული</h3>
    <div
      class="flex flex-col mt-5 gap-3 h-[250px] lg:h-[520px] scroll-smooth overflow-y-scroll"
    >
      <div v-for="data in popularListData" :key="data.id">
        <div class="flex gap-1 items-center">
          <img :src="data.src" alt="photo" />
          <p class="text-sm">
            {{ data.about }}
          </p>
        </div>
        <hr class="border-dashed border-2 border-background mt-3" />
      </div>
    </div>
  </div>
</template>
