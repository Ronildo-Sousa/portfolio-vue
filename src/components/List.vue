<script setup>
import Card from "./Card.vue";

const props = defineProps({
  projects: Array,
  title: String,
  id: String,
});
</script>

<template>
  <div class="relative rounded group">
    <h1 :id="id" class="mt-5 mb-5 ml-3 text-3xl font-medium text-gray-200">{{ title ?? "Title" }}</h1>
    <div class="overflow-x-scroll cursor-pointer scrollbar-thin scrollbar-thumb-blue-700 hover:scrollbar-thumb-blue-500 scrollbar-thumb-rounded-full">
      <div
        class="transition duration-500 ease-in-out"
        :style="{width: projects.length * 400 + 'px' }"
        v-if="projects"
      >
        <Card
          class="inline-block mb-5"
          v-for="(project, idx) in projects"
          :key="idx"
          :image="project.image"
          :title="project.title"
          :description="project.description"
          :link="project.link"
          :link_text="'Ver Detalhes'"
        />
      </div>
    </div>
  </div>
</template>
