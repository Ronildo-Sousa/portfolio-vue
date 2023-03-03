<script setup>
import { ref } from "vue";
import MenuItem from "./MenuItem.vue";
let open = ref(false);
let activePage = ref("Home");
</script>

<template>
  <nav
    class="fixed top-0 left-0 right-0 z-10 border-b border-indigo-900 bg-gradient-to-r from-black to-gray-600"
  >
    <div class="px-2 mx-auto max-w-7xl sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <button
            type="button"
            @click="open = !open"
            class="inline-flex items-center justify-center p-2 text-gray-400 rounded-md hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
            aria-controls="mobile-menu"
            aria-expanded="false"
          >
            <span class="sr-only">Open main menu</span>

            <svg
              :class="[open ? 'hidden' : 'block']"
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>

            <svg
              :class="[open ? 'block' : 'hidden']"
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
        <div
          class="flex items-center justify-center flex-1 sm:items-stretch sm:justify-between"
        >
          <div class="flex w-[60px] items-center flex-shrink-0">
            <a href="/">
              <img  src="../assets/logo.png" alt="Your Company" />
            </a>
          </div>
          <div class="items-center hidden sm:ml-6 sm:flex">
            <div class="flex space-x-4">
              <MenuItem
                @click="activePage = 'Home'"
                text="Home"
                url="#home"
                :active="activePage"
              />
              <MenuItem
                :text="'Projetos'"
                :url="'#projetos'"
                :active="activePage"
                @click="activePage = 'Projetos'"
              />
              <MenuItem
                :text="'Habilidades'"
                :url="'#habilidades'"
                :active="activePage"
                @click="activePage = 'Habilidades'"
              />
            </div>
          </div>
          <div></div>
        </div>
      </div>
    </div>

    <div :class="[open ? 'block' : 'hidden']" class="sm:hidden" id="mobile-menu">
      <div class="px-2 pt-2 pb-3 space-y-1 text-center">
        <MenuItem
          :text="'Home'"
          :url="'#home'"
          :active="activePage"
          @click="activePage = 'Home'"
        />
        <MenuItem
          :text="'Projetos'"
          :url="'#projetos'"
          :active="activePage"
          @click="activePage = 'Projetos'"
        />
        <MenuItem
          :text="'Habilidades'"
          :url="'#habilidades'"
          :active="activePage"
          @click="activePage = 'Habilidades'"
        />
      </div>
    </div>
  </nav>
</template>
