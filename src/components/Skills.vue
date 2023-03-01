<script setup>
import CardSkill from "./CardSkill.vue";
const props = defineProps({
  id: String,
  title: String,
  skills: Array,
});
</script>

<template>
  <section class="mt-10 mb-5">
    <h1 :id="id" class="mb-8 ml-2 text-3xl font-medium">{{ title ?? "Title" }}</h1>
    <div class="flex justify-around gap-4 flex-wrap">
      <CardSkill
        v-for="(skill, idx) in skills"
        :key="idx"
        :defaultImage="skill.defaultImage"
        :name="skill.name"
      />
    </div>
  </section>
</template>
