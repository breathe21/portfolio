<script setup>
import { ref } from "vue";

const openBar = ref(false);

const handleShowBarMobile = () => {
  openBar.value = !openBar.value;
};
</script>

<template>
  <header class="container mx-auto px-4">
    <nav class="flex justify-between items-center py-8">
      <div>
        <h1 class="text-4xl font-light text-center">Breathe</h1>
      </div>
      <div class="md:hidden relative">
        <i
          class="fa-solid fa-bars text-2xl cursor-pointer p-2"
          @click="handleShowBarMobile"
        ></i>
        <ul
          v-if="openBar"
          class="justify-center space-x-4 text-xl bg-gray-300 absolute top-full right-0 rounded-2xl"
        >
          <li
            class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
          >
            <a href="#about">About</a>
          </li>
          <li
            class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
          >
            <a href="#experience">Experience</a>
          </li>
          <li
            class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
          >
            <a href="#projects">Projects</a>
          </li>
          <li
            class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
          >
            <a href="#contact">Contact</a>
          </li>
        </ul>
      </div>
      <ul class="hidden md:flex justify-center space-x-4 text-xl">
        <li
          class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
        >
          <a href="#about">About</a>
        </li>
        <li
          class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
        >
          <a href="#experience">Experience</a>
        </li>
        <li
          class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
        >
          <a href="#projects">Projects</a>
        </li>
        <li
          class="p-2 hover:text-amber-400 hover:transition hover:duration-300 hover:ease-in-out cursor-pointer"
        >
          <a href="#contact">Contact</a>
        </li>
      </ul>
    </nav>
  </header>
</template>