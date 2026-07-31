<script setup>

  defineProps(['title', 'items']);
  
</script>
<template>
  <div class="rounded-2xl text-center py-4 border">
    <h1 class="font-bold text-2xl mt-2 text-gray-700">{{ title }}</h1>
    <div class="grid grid-cols-2 gap-4 mt-4 py-5 px-10 space-y-4 ">
      <div class="flex gap-4" v-for="item in items">
        <i class="fa-solid fa-circle-check text-lg"></i>
        <div class="text-left">
          <h6 class="font-bold text-gray-700 text-lg">{{ item }}</h6>
        <p class="text-sm text-gray-500">Experienced</p>
        </div>
      </div>
    </div>
  </div>
</template>