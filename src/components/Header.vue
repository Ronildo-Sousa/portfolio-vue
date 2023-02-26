<script setup>
import { ref } from "vue";
import MenuItem from "./MenuItem.vue";
let open = ref(true);
let activePage = ref("Projetos");
</script>

<template>
  <nav class="">
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
          <div class="flex items-center flex-shrink-0">
            <a href="/">
              <img class="block w-auto h-8" src="../assets/logo.svg" alt="Your Company" />
            </a>
          </div>
          <div class="hidden sm:ml-6 sm:block">
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
      </div>
    </div>
  </nav>
</template>
