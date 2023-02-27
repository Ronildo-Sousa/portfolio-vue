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
    <div class="overflow-x-scroll">
      <div
        class="transition duration-500 ease-in-out"
        :style="{width: projects.length * 400 + 'px' }"
        v-if="projects"
      >
        <Card
          class="inline-block mb-3"
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
