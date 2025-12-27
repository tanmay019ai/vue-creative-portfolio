<script setup lang="ts">
import github from "@/assets/social/github.png"
import linkedin from "@/assets/social/linkedln.png"
import leetcode from "@/assets/social/leetcode.png"
import gfg from "@/assets/social/geeksforgeeks.png"
import youtube from "@/assets/social/youtube.png"

const profiles = [
  {
    name: "GitHub",
    url: "https://github.com/tanmay019ai",
    icon: github,
  },
  {
    name: "LinkedIn",
    url: "https://www.linkedin.com/in/tanmay-srivastav-56009b32b/",
    icon: linkedin,
  },
  {
    name: "LeetCode",
    url: "https://leetcode.com/u/tanmay019/",
    icon: leetcode,
  },
  {
    name: "GeeksforGeeks",
    url: "https://www.geeksforgeeks.org/profile/tanmayh16u",
    icon: gfg,
  },
  {
    name: "YouTube",
    url: "https://www.youtube.com/@thetanmay6750",
    icon: youtube,
  },
]
</script>

<template>
  <section class="bg-black text-white py-28 px-4 sm:px-6">
    <div class="max-w-6xl mx-auto">

      <!-- TITLE -->
      <h2 class="text-3xl sm:text-4xl font-semibold text-center">
        Online Presence
      </h2>

      <p class="mt-4 text-neutral-400 text-center max-w-3xl mx-auto">
        I actively build, solve problems, and share my learning across platforms.
      </p>

      <!-- LOGO GRID -->
      <div class="mt-12 flex flex-wrap justify-center gap-10">
        <a
          v-for="p in profiles"
          :key="p.name"
          :href="p.url"
          target="_blank"
          class="group flex flex-col items-center gap-2"
        >
          <div
            class="w-16 h-16 bg-white rounded-xl flex items-center justify-center
                   group-hover:scale-105 transition"
          >
            <img
              :src="p.icon"
              :alt="p.name"
              class="w-8 h-8 object-contain"
            />
          </div>
          <span class="text-sm text-neutral-400">
            {{ p.name }}
          </span>
        </a>
      </div>

      <!-- RESUME EMBED -->
      <div class="mt-20">
        <h3 class="text-2xl font-semibold text-center mb-6">
          Resume
        </h3>

        <div
          class="w-full max-w-4xl mx-auto border border-white/10 rounded-xl overflow-hidden"
        >
          <iframe
            src="/resume.pdf"
            class="w-full h-[600px]"
            frameborder="0"
          ></iframe>
        </div>

        <p class="mt-4 text-center text-sm text-neutral-500">
          Scroll to view · Download using browser controls
        </p>
      </div>

    </div>
  </section>
</template>
