<script setup>
import List from './components/List.vue'
const projects = [
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
  {
    "title": 'Short Url',
    'description': "É um simples encurtador de urls desenvolvido utilizando- se testes automatizados,Livewire e Tailwind, nesta aplicação o usuário pode criar e gerenciar uma url curta, podendo observar o desempenho de visualizações diárias, semanais, etc...",
    'image': 'https://picsum.photos/seed/picsum/400/300',
    'link': 'https://github.com/Ronildo-Sousa/short-url'
  },
]
</script>

<template>
  <div class="text-white bg-gradient-to-r from-black to-gray-600">
    <List :projects="projects" />
  </div>
</template>