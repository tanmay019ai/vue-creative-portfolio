<script setup lang="ts">
const experiences = [
  {
    role: "Open Source Developer",
    company: "GirlScript Summer of Code",
    duration: "Sep 2024 – Dec 2024",
    logo: "/logos/girlscriptsoc_logo.png",
    points: [
      "Contributed to real-world open source projects",
      "Collaborated with global developers",
      "Improved code quality and features",
    ],
  },
  {
    role: "Frontend Developer Intern",
    company: "SheenEdge",
    duration: "Feb 2025 – Jul 2025",
    logo: "/logos/sheenedge.png",
    points: [
      "Built responsive HTML email templates",
      "Worked with React for UI development",
      "Improved frontend performance",
    ],
  },
  {
    role: "Open Source Developer",
    company: "Open Source Connect India",
    duration: "Aug 2025 – Oct 2025",
    logo: "/logos/open_source_connect_logo.png",
    points: [
      "Selected contributor for national OSS initiative",
      "Collaborated on impactful open-source software",
      "Strengthened teamwork and problem-solving",
    ],
  },
  {
    role: "Full Stack Developer Intern",
    company: "Last Minutes Deal",
    duration: "Oct 2025 – Nov 2025",
    logo: "/logos/last_minutes_deal_logo.png",
    points: [
      "Improved backend CSV processing modules",
      "Optimized frontend performance",
      "Fixed bugs and enhanced UX",
    ],
  },
  {
    role: "Growth Partner",
    company: "Parikshak.ai",
    duration: "Aug 2025 – Present",
    logo: "/logos/parikshak_ai_logo.png",
    points: [
      "Promoted AI-driven hiring tools on campus",
      "Organized onboarding drives",
      "Helped students from resume to offer",
    ],
  },
]
</script>

<template>
  <section id="experience" class="bg-black text-white py-28 px-4 sm:px-6">
    <div class="max-w-5xl mx-auto">

      <!-- HEADER -->
      <h2 class="text-4xl font-semibold text-center">
        Experience
      </h2>
      <p class="mt-4 text-neutral-400 text-center max-w-2xl mx-auto">
        My professional and technical journey over time
      </p>

      <!-- VERTICAL TIMELINE -->
      <div class="mt-20 flex flex-col items-center space-y-14">

        <div
          v-for="(exp, i) in experiences"
          :key="i"
          class="w-full flex flex-col items-center"
        >
          <!-- CARD -->
          <div
            class="w-full md:w-[720px] bg-white/5 backdrop-blur-xl
                   border border-white/15 rounded-3xl p-8
                   shadow-[0_0_60px_rgba(255,255,255,0.08)]
                   hover:shadow-[0_0_90px_rgba(255,255,255,0.15)]
                   transition"
          >
            <!-- LOGO -->
            <div class="w-14 h-14 bg-white rounded-xl p-2 mb-5">
              <img
                :src="exp.logo"
                :alt="exp.company"
                class="w-full h-full object-contain"
              />
            </div>

            <h3 class="text-xl font-semibold">
              {{ exp.role }}
            </h3>
            <p class="text-sm text-neutral-300">
              {{ exp.company }}
            </p>
            <p class="text-xs text-neutral-500 mb-5">
              {{ exp.duration }}
            </p>

            <ul class="space-y-2 text-sm text-neutral-400">
              <li v-for="(p, j) in exp.points" :key="j">
                • {{ p }}
              </li>
            </ul>
          </div>

          <!-- DOWN ARROW -->
          <div
            v-if="i !== experiences.length - 1"
            class="text-neutral-500 text-4xl mt-10"
          >
            ↓
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
