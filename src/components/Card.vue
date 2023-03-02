<script setup>
import MyButton from "./MyButton.vue";
const props = defineProps({
  image: String,
  title: String,
  description: String,
  link: String,
  link_text: String,
});
</script>

<template>
  <div
    class="w-[400px] h-[500px] flex flex-col max-w-sm mx-auto lg:max-w-md overflow-hidden bg-gray-900 rounded-lg cursor-pointer bg-gradient-to-b from-gray-700 to-gray-900 hover:from-gray-900 hover:to-gray-700"
  >
    <div class="flex-grow-0 h-[200px] basis-auto">
      <img
        class="object-fill w-full h-full rounded"
        :src="image ?? 'https://picsum.photos/seed/picsum/400/300'"
        alt="card-item"
      />
    </div>
    <div class="flex flex-col items-center justify-center flex-grow p-6 basis-auto">
      <h1 class="mb-3 text-xl font-medium">{{ title }}</h1>
      <p class="mb-3 text-center break-words">
        {{ description }}
      </p>
      <MyButton :uri="link">
        {{ link_text }}
      </MyButton>
    </div>
  </div>
</template>
