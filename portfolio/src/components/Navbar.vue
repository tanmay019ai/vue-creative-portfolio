<script setup lang="ts">
import { ref } from "vue"

const open = ref(false)

const links = [
  { name: "Home", href: "#home" },
  { name: "Tech Stack", href: "#tech-stack" },
  { name: "Online Presence", href: "#online-presence" },
  { name: "Freelance", href: "#freelance" },
  { name: "Experience", href: "#experience" },
]
</script>

<template>
  <header
    class="fixed top-0 left-0 w-full z-50
           bg-black/70 backdrop-blur-xl
           border-b border-white/10"
  >
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <!-- NAV BAR -->
      <div class="h-12 flex items-center justify-end relative">

        <!-- DESKTOP NAV -->
        <nav
          class="hidden md:flex gap-10
                 text-sm text-neutral-300"
        >
          <a
            v-for="l in links"
            :key="l.name"
            :href="l.href"
            class="hover:text-white transition"
          >
            {{ l.name }}
          </a>
        </nav>

        <!-- MOBILE MENU BUTTON -->
        <button
          class="md:hidden text-white text-xl ml-2"
          @click="open = !open"
          aria-label="Menu"
        >
          ☰
        </button>

        <!-- MOBILE DROPDOWN -->
        <div
          v-if="open"
          class="absolute top-12 right-0
                 w-48
                 bg-black/95 backdrop-blur-xl
                 border border-white/10
                 rounded-lg
                 shadow-xl"
        >
          <nav class="flex flex-col py-2">
            <a
              v-for="l in links"
              :key="l.name"
              :href="l.href"
              class="px-4 py-2 text-sm text-neutral-300
                     hover:bg-white/5 hover:text-white transition"
              @click="open = false"
            >
              {{ l.name }}
            </a>
          </nav>
        </div>

      </div>
    </div>
  </header>
</template>
