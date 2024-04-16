<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue';
import { Icon } from '@iconify/vue';
</script>
<template>
  <Menu as="div" class="relative inline-block text-left">
    <div>
      <MenuButton
        class="inline-flex w-full items-center justify-center gap-x-1.5 rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 ring-gray-300 hover:text-blue"
      >
        სხვა
        <Icon icon="ic:baseline-keyboard-arrow-down" width="20" />
      </MenuButton>
    </div>

    <transition
      enter-active-class="transition ease-out duration-100"
      enter-from-class="transform opacity-0 scale-95"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-75"
      leave-from-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-95"
    >
      <MenuItems
        class="absolute right-[-100px] z-10 mt-2 w-44 origin-top-right rounded-xl bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
      >
        <div>
          <MenuItem v-slot="{ active }">
            <a
              href="#"
              :class="[
                active ? 'bg-primaryLight text-blue' : 'text-grey',
                'block px-4 py-4  rounded-xl text-base font-medium  lg:hidden',
              ]"
            >
              ბიზნესი & ეკონომიკა</a
            >
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <a
              href="#"
              :class="[
                active ? 'bg-primaryLight text-blue' : 'text-grey',
                'block px-4 py-4  rounded-xl text-base font-medium',
              ]"
              >მსოფლიო</a
            >
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <a
              href="#"
              :class="[
                active ? 'bg-primaryLight text-blue' : 'text-grey',
                'block px-4 py-4  rounded-xl text-base font-medium',
              ]"
              >ხელოვნება</a
            >
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <a
              href="#"
              :class="[
                active ? 'bg-primaryLight text-blue' : 'text-grey',
                'block px-4 py-4  rounded-xl text-base font-medium',
              ]"
              >სპორტი</a
            >
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <a
              href="#"
              :class="[
                active ? 'bg-primaryLight text-blue' : 'text-grey',
                'block px-4 py-4  rounded-xl text-base font-medium',
              ]"
              >რელიგია</a
            >
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <a
              href="#"
              :class="[
                active ? 'bg-primaryLight text-blue' : 'text-grey',
                'block px-4 py-4  rounded-xl text-base font-medium',
              ]"
              >კრიმინალი</a
            >
          </MenuItem>
        </div>
      </MenuItems>
    </transition>
  </Menu>
</template>
