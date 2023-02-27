<script setup>
import { onMounted } from "vue";
import axios from "axios";
import List from "./components/List.vue";
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";

onMounted(() => {
  // const request = axios
  //   .create({
  //     headers: {
  //       Accept: "application/vnd.github+json",
  //       Authorization: `Bearer ${import.meta.env.VITE_GITHUB_TOKEN}`,
  //     },
  //   })
  //   .get("https://api.github.com/users/Ronildo-Sousa/repos")
  //   .then((response) => {
  //     console.log(response);
  //   });
});
const projects = [
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
  {
    title: "Short Url",
    description:
      "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    image: "https://picsum.photos/seed/picsum/400/300",
    link: "https://github.com/Ronildo-Sousa/short-url",
  },
];

const personalInformation = {
  name: "Ronildo Sousa",
  title: "Full Stack PHP/Laravel",
  description:
    "Desenvolvedor iniciante Full Stack com forte paixão por tecnologia e habilidades comprovadas em desenvolvimento de software. Com aproximadamente 2 anos de experiência em projetos pessoais em Laravel, tenho conhecimento sólido em PHP, HTML, CSS, JavaScript e em outras ferramentas como Git e MySQL. Sou familiarizado com aplicações web, tanto frontend quanto backend. Busco constantemente aprender e aprimorar minhas habilidades, e estou animado para dar meus primeiros passos como desenvolvedor profissional. Acredito que posso trazer entusiasmo, dedicação e soluções criativas para equipes de desenvolvimento e contribuir para o sucesso dos projetos.",
  image: "https://avatars.githubusercontent.com/u/60019987?v=4",
  social_links: [
    { text: "Github", url: "https://github.com/Ronildo-Sousa" },
    { text: "LinkedIn", url: "https://linkedin.com/in/ronildosousa" },
  ],
};
</script>

<template>
  <div class="px-8 text-white bg-gradient-to-r from-black to-gray-600">
    <div class="max-w-6xl py-3 mx-auto">
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
    </div>
  </div>
</template>
