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
  <section id="online-presence" class="bg-black text-white py-20 px-4 sm:px-6">
    <div class="max-w-6xl mx-auto">

      <!-- TWO-COLUMN GRID (CONTROLLED GAP) -->
      <div
        class="grid grid-cols-[1fr_auto]
               gap-6 sm:gap-8 md:gap-10
               items-start"
      >

        <!-- LEFT: ONLINE PRESENCE -->
        <div>
          <h2 class="text-2xl sm:text-3xl font-semibold">
            Online Presence
          </h2>

          <p class="mt-3 text-sm sm:text-base text-neutral-400 max-w-md">
            I actively build, solve problems, and share my learning across platforms.
          </p>

          <!-- LOGOS -->
          <div class="mt-8 flex flex-wrap gap-5">
            <a
              v-for="p in profiles"
              :key="p.name"
              :href="p.url"
              target="_blank"
              class="group flex flex-col items-center gap-1"
            >
              <div
                class="w-12 h-12 sm:w-14 sm:h-14
                       bg-white rounded-xl flex items-center justify-center
                       group-hover:scale-105 transition"
              >
                <img
                  :src="p.icon"
                  :alt="p.name"
                  class="w-6 h-6 sm:w-7 sm:h-7 object-contain"
                />
              </div>
              <span class="text-[11px] sm:text-xs text-neutral-400">
                {{ p.name }}
              </span>
            </a>
          </div>
        </div>

        <!-- RIGHT: RESUME -->
        <div class="flex flex-col items-center">
          <h3 class="text-lg sm:text-xl font-semibold mb-4">
            Resume
          </h3>

          <div
            class="bg-white border border-white/10 rounded-lg
                   overflow-hidden
                   w-[180px] sm:w-[220px] md:w-[260px]"
          >
            <img
              src="@/assets/resume/resume-preview.png"
              alt="Resume Preview"
              class="w-full h-auto object-contain"
            />
          </div>

          <div class="mt-4">
            <a
              href="/resume.pdf"
              download
              class="inline-block px-5 py-2 bg-white text-black rounded-md
                     text-sm font-medium hover:bg-neutral-200 transition"
            >
              Download
            </a>
          </div>
        </div>

      </div>

    </div>
  </section>
</template>
