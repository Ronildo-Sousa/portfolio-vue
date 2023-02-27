<script setup>
import MyButton from "./MyButton.vue";

const props = defineProps({
  name: String,
  title: String,
  description: String,
  social_links: Array,
  image: String,
  id: String,
});
</script>

<template>
  <div :id="id" class="flex items-center justify-center py-10">
    <div class="flex flex-col items-center max-w-2xl text-center md:items-start md:text-start max-w-2x">
      <h1
        class="text-3xl font-bold tracking-tight text-transparent bg-clip-text bg-gradient-to-r from-emerald-300 to-blue-400 sm:text-5xl"
      >
        {{ name }}
      </h1>
      <h3 class="mt-1 text-gray-300">
        {{ title }}
      </h3>

      <p class="mt-6 mb-6 text-lg leading-8 text-gray-400">
        {{ description }}
      </p>
      <div>
        <MyButton v-for="(social, idx) in social_links" :key="idx" :uri="social.url">
          {{ social.text }}
        </MyButton>
      </div>
    </div>
    <div class="items-center justify-end hidden lg:flex">
      <img :src="image" class="rounded-md w-[60%]" alt="profile_pic" />
    </div>
  </div>
</template>
