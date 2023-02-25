<script>
import Card from './Card.vue'
export default {
    props: {
        projects: Array
    },
    components:{
        Card
    }
}
</script>

<template>
    <div class="overflow-x-hidden px-8">
        <div class="w-[99999px]">
            <div class="inline-block" v-if="projects" v-for="project in projects">
                <Card
                :image="project.image"
                :title="project.title"
                :description="project.description"
                :link="project.link"
                :link_text="'Ver Detalhes'" />
            </div>
        </div>
    </div>
</template>