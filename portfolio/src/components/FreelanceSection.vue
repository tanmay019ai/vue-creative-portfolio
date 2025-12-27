<script setup lang="ts">
import webdokImg from "@/assets/webdok-logo.png"

// 🔗 Replace this with YOUR real Freelancer.com profile link
const freelancerProfile =
  "https://www.freelancer.com/u/tanmaysr56"
</script>

<template>
  <section id="freelance" class="bg-black text-white py-28 px-4 sm:px-6">
    <div class="max-w-5xl mx-auto">

      <!-- TITLE -->
      <h2 class="text-3xl sm:text-4xl font-semibold text-center">
        Freelance Experience
      </h2>

      <p class="mt-4 text-neutral-400 text-center max-w-xl mx-auto">
        Over 1+ year of hands-on freelance experience working on real-world systems.
      </p>

      <!-- CONTENT -->
      <div class="mt-16 grid grid-cols-1 md:grid-cols-2 gap-12 items-center">

        <!-- COMPANY IMAGE -->
        <div class="flex justify-center">
          <img
            :src="webdokImg"
            alt="Webdok"
            class="w-full max-w-md rounded-xl border border-white/10"
          />
        </div>

        <!-- WORK DETAILS -->
        <div>
          <h3 class="text-2xl font-medium">
            Freelance Developer — Webdok
          </h3>

          <p class="mt-4 text-neutral-400 leading-relaxed">
            I worked as a freelance developer on paid client projects,
            contributing to real production systems and internal tools.
          </p>

          <ul class="mt-6 space-y-3 text-sm text-neutral-300">
            <li>• Built and maintained web-based systems for clients</li>
            <li>• Developed application features based on real requirements</li>
            <li>• Collaborated with team members on paid freelance work</li>
            <li>• Delivered production-ready code and updates</li>
          </ul>

          <!-- FREELANCER PROFILE -->
          <div class="mt-8">
            <a
              :href="freelancerProfile"
              target="_blank"
              class="inline-block text-sm underline underline-offset-4
                     hover:text-white"
            >
              View my Freelancer.com profile →
            </a>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
