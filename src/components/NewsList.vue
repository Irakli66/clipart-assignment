<script setup>
import { Icon } from '@iconify/vue';

const newsData = [
  {
    id: 1,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 2,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 3,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 4,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 5,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 6,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 7,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 8,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 9,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 10,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 11,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 12,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 13,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 14,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 15,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 16,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 17,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 18,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 19,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
  {
    id: 20,
    time: '7:30',
    date: '02.01.2023',
    about: 'დღეიდან ასაწონად განკუთვნილი პოლიეთილენის პარკები აიკრძალა',
  },
];
</script>

<template>
  <div class="h-[330px] lg:h-[606px] p-5 2xl:w-[300px] bg-white rounded-2xl">
    <h3 class="font-bold text-xl">ყველა სიახლე</h3>
    <div
      class="flex flex-col mt-5 gap-3 h-[250px] lg:h-[520px] scroll-smooth overflow-y-scroll"
    >
      <div class="flex-col gap-x-5" v-for="data in newsData" :key="data.id">
        <div class="flex items-center gap-2">
          <Icon icon="mdi:clock-outline" color="#585ee2" />
          <p class="text-blue text-sm">{{ data.time }}</p>
          <p class="text-blue text-sm">{{ data.date }}</p>
        </div>
        <p class="text-sm">
          {{ data.about }}
        </p>
        <hr class="border-dashed border-2 border-background mt-3" />
      </div>
    </div>
  </div>
</template>
