<script setup>
const props = defineProps({
  email: String,
  linkedin: String,
  github: String,
});
</script>

<template>
  <footer class="p-2 text-white bg-gradient-to-l from-gray-700 to-gray-900">
    <div class="flex items-center justify-around gap-5">
      <div class="w-[60px]">
        <a href="/">
          <img src="../assets/logo.png" alt="logo" />
        </a>
      </div>
      
      <div class="flex flex-col h-[70px] justify-end font-bold">
        <p>© Ronildo Sousa - 2023</p>
      </div>
      <div class="flex flex-col gap-1">
        <a :href="'mailto:' + email" class="hover:underline">Email</a>
        <a :href="linkedin" class="hover:underline">LinkedIn</a>
        <a :href="github" class="hover:underline">Github</a>
      </div>
    </div>
  </footer>
</template>
