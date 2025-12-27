<script setup lang="ts">
import p1 from "@/assets/projects/1.png"
import p2 from "@/assets/projects/2.png"
import p3 from "@/assets/projects/3.png"
import p4 from "@/assets/projects/4.png"
import p5 from "@/assets/projects/5.png"

const featuredProjects = [
  {
    id: 1,
    title: "Codeminds Student Panel",
    desc: "Student dashboard system with admin & student workflows.",
    tech: "TypeScript · Web App",
    github: "https://github.com/tanmay019ai/codeminds-student-panel",
    live: "https://codeminds-student-panel.vercel.app",
    image: p1,
  },
  {
    id: 2,
    title: "Webdok Portfolio Client",
    desc: "Client portfolio website built for Webdok.",
    tech: "TypeScript · Frontend",
    github: "https://github.com/tanmay019ai/Webdok_portfolio-client-",
    live: "https://webdok-portfolio-client.vercel.app",
    image: p2,
  },
  {
    id: 3,
    title: "Defender Showcase (3D)",
    desc: "3D interactive showcase using Three.js and Tailwind.",
    tech: "React · Tailwind · Three.js",
    github: "https://github.com/tanmay019ai/defender-showcase",
    live: "https://defender-3d.vercel.app",
    image: p3,
  },
  {
    id: 4,
    title: "Medicare – Hospital Website",
    desc: "Medical-themed hospital management UI website.",
    tech: "JavaScript · UI",
    github: "https://github.com/tanmay019ai/Medicare",
    live: "https://medicare-theta-lovat.vercel.app",
    image: p4,
  },
  {
    id: 5,
    title: "Planora – AI Home Designer",
    desc: "AI-powered platform that generates 3D home designs from prompts.",
    tech: "AI · 3D · Web",
    github: "https://github.com/tanmay019ai/planora-ai-home-designer",
    live: "https://planora-ai-home-designer.vercel.app",
    image: p5,
  },
]
</script>

<template>
  <section
    id="featured-work"
    class="bg-black text-white py-28 px-4 sm:px-6"
  >
    <div class="max-w-6xl mx-auto">

      <!-- TITLE -->
      <h2 class="text-3xl sm:text-4xl font-semibold text-center">
        Featured Projects
      </h2>

      <p class="mt-4 text-neutral-400 text-center max-w-xl mx-auto">
        Real projects deployed on production, including freelance and system-level work.
      </p>

      <!-- GRID -->
      <div class="mt-16 grid grid-cols-1 md:grid-cols-2 gap-8">
        <div
          v-for="project in featuredProjects"
          :key="project.id"
          class="group border border-white/10 rounded-xl overflow-hidden
                 hover:border-white/30 transition"
        >
          <!-- IMAGE -->
          <div class="h-48 overflow-hidden bg-neutral-900">
            <img
              :src="project.image"
              :alt="project.title"
              class="w-full h-full object-cover
                     group-hover:scale-105 transition duration-500"
            />
          </div>

          <!-- CONTENT -->
          <div class="p-6">
            <h3 class="text-lg font-medium">
              {{ project.id }}. {{ project.title }}
            </h3>

            <p class="mt-2 text-sm text-neutral-400">
              {{ project.desc }}
            </p>

            <p class="mt-3 text-xs text-neutral-500">
              {{ project.tech }}
            </p>

            <!-- LINKS -->
            <div class="mt-4 flex gap-4 text-sm">
              <a
                :href="project.github"
                target="_blank"
                class="underline underline-offset-4 hover:text-white"
              >
                GitHub
              </a>

              <a
                :href="project.live"
                target="_blank"
                class="underline underline-offset-4 hover:text-white"
              >
                Live Preview
              </a>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>
