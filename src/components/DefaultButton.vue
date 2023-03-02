<script setup>
const props = defineProps({
  uri: String,
});
</script>

<template>
  <a
    :href="uri ?? '#'"
    target="_blanck"
    class="p-2 mr-3 font-medium text-white rounded-full px-7 bg-gradient-to-r from-indigo-600 to-emerald-400 hover:from-indigo-600 hover:to-indigo-800"
  >
    <slot> meu botão </slot>
  </a>
</template>
