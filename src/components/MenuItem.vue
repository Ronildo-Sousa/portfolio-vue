<script setup>
const props = defineProps({
  url: String,
  text: String,
  active: String,
});
</script>

<template>
  <a
    :href="url"
    :class="[
      active === text
        ? 'underline underline-offset-8 decoration-2 decoration-indigo-500 text-white hover:text-gray-500'
        : '',
    ]"
    class="block px-3 py-2 text-base text-gray-400 cursor-pointer hover:text-white"
    aria-current="page"
  >
    {{ text }}
  </a>
</template>
