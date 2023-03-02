<script setup>
const props = defineProps({
  email: String,
  linkedin: String,
  github: String,
});
</script>

<template>
  <footer class="bg-gradient-to-l text-white from-gray-700 to-gray-900 p-2">
    <div class="flex items-center justify-around gap-5">
      <div class="w-[40px]">
        <a href="/">
          <img src="../assets/logo.svg" alt="logo" />
        </a>
      </div>

      <div class="flex flex-col gap-1">
        <a :href="'mailto:' + email" class="hover:underline">Email</a>
        <a :href="linkedin" class="hover:underline">LinkedIn</a>
        <a :href="github" class="hover:underline">Github</a>
      </div>
    </div>
    <div class="text-center">© Ronildo Sousa - 2023</div>
  </footer>
</template>
