<script setup>
const props = defineProps({
  name: String,
  defaultImage: String,
});
</script>

<template>
  <div
    class="w-[160px] border-2 border-transparent hover:border-blue-600 cursor-pointer p-2 group rounded-md flex flex-col items-center bg-gradient-to-tl from-gray-600 to-gray-900 text-white"
  >
    <div class="w-[65%] mt-3">
      <div>
        <img :src="defaultImage" alt="habilidade" />
      </div>
    </div>
    <div class="text-lg font-medium mt-2 text-center">
      <p>{{ name }}</p>
    </div>
  </div>
</template>
