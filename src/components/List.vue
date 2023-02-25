<script setup>
import { ref } from 'vue'
import Card from './Card.vue'

const ScrollX = ref(0)

const props = defineProps({
    projects: Array
})

function handleLeft() {
    let x = ScrollX.value + Math.round(window.innerWidth / 2)
    if (x > 0) {
        x = 0
    }
    ScrollX.value = x
}

function handleRight() {
    let x = ScrollX.value - Math.round(window.innerWidth / 2);
    let listW = props.projects.length * 400;
    if ((window.innerWidth - listW) > x) {
        x = ((window.innerWidth - listW) - 60);
    }
    ScrollX.value = x
}
</script>

<template>
    <div class="relative rounded group bg-gradient-to-tr from-blue-600">
        <div @click="handleLeft"
            class="absolute h-[80%] top-16 flex items-center group-hover:opacity-100 hover:text-blue-400 opacity-0 left-0 cursor-pointer transition ease-in-out duration-300 overflow-hidden ml-3">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                class="w-8 h-8">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
            </svg>
        </div>
        <div @click="handleRight"
            class="absolute h-[80%] top-16 flex items-center right-0 cursor-pointer group-hover:opacity-100 hover:text-blue-400 opacity-0 transition ease-in-out duration-300 overflow-hidden">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                class="w-8 h-8">
                <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
            </svg>
        </div>
        <div class="overflow-x-hidden">
            <div class="transition duration-500 ease-in-out"
                :style="{ marginLeft: ScrollX + 'px', width: projects.length * 400 + 'px' }" v-if="projects">
                <Card class="inline-block" v-for="(project, idx) in projects" :key="idx" :image="project.image"
                    :title="project.title" :description="project.description" :link="project.link"
                    :link_text="'Ver Detalhes'" />
            </div>
        </div>
    </div>
</template>