<script setup>
import List from "./components/List.vue";
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Skills from "./components/Skills.vue";
import Footer from "./components/Footer.vue";
import personalInformation from "./data/personalInformation.json";
import projects from "./data/projects.json";
import skills from "./data/skills.json";
</script>

<template>
  <div class="px-8 text-white bg-gradient-to-r from-black to-gray-600">
    <div class="flex flex-col max-w-6xl gap-10 py-10 mx-auto">
      <Header />
      <Hero
        :id="'home'"
        :name="personalInformation.name"
        :title="personalInformation.title"
        :description="personalInformation.description"
        :image="personalInformation.image"
        :social_links="personalInformation.social_links"
      />
      <List :id="'projetos'" :projects="projects" title="Meus projetos" />
      <Skills :id="'habilidades'" title="Minhas Habilidades" :skills="skills" />
    </div>
  </div>
  <Footer
    :email="personalInformation.email"
    :linkedin="personalInformation.social_links[1].url"
    :github="personalInformation.social_links[0].url"
  />
</template>
