<script setup lang="ts">
</script>

<template>
  <section id="contact" class="relative bg-black text-white py-28 px-4 sm:px-6 overflow-hidden">
    <div class="max-w-6xl mx-auto relative z-10">

      <!-- SECTION HEADER -->
      <h2 class="text-4xl font-semibold text-center">
        Let’s Work Together
      </h2>
      <p class="mt-4 text-neutral-400 text-center max-w-2xl mx-auto">
        Open to meaningful opportunities, collaborations, and challenging projects.
      </p>

      <!-- MAIN GRID -->
      <div
        class="mt-20 grid grid-cols-1 md:grid-cols-2 gap-12 items-start"
      >

        <!-- LEFT: AVAILABILITY -->
        <div
          class="bg-white/5 backdrop-blur-xl
                 border border-white/15 rounded-3xl p-8
                 shadow-[0_0_60px_rgba(255,255,255,0.08)]"
        >
          <h3 class="text-2xl font-semibold mb-6">
            I’m Available For
          </h3>

          <ul class="space-y-4 text-neutral-300 text-sm">
            <li class="flex gap-3">
              <span class="text-xl">🚀</span>
              <span>
                <strong>Freelance Projects</strong> – Web apps, dashboards, AI-powered systems
              </span>
            </li>

            <li class="flex gap-3">
              <span class="text-xl">💼</span>
              <span>
                <strong>Full-time / Internship Roles</strong> – Software Engineer, Web / AI roles
              </span>
            </li>

            <li class="flex gap-3">
              <span class="text-xl">🤝</span>
              <span>
                <strong>Collaborations</strong> – Startups, open-source, hackathons
              </span>
            </li>

            <li class="flex gap-3">
              <span class="text-xl">🧠</span>
              <span>
                <strong>AI & Agentic Systems</strong> – Chat agents, RAG, automation
              </span>
            </li>
          </ul>
        </div>

        <!-- RIGHT: CONTACT -->
        <div
          class="relative bg-white/5 backdrop-blur-xl
                 border border-white/15 rounded-3xl p-8
                 shadow-[0_0_60px_rgba(255,255,255,0.08)]"
        >
          <h3 class="text-2xl font-semibold mb-4">
            Get In Touch
          </h3>

          <p class="text-sm text-neutral-400 mb-8">
            Have an idea or opportunity? Let’s talk and build something impactful.
          </p>

          <a
  href="https://mail.google.com/mail/?view=cm&to=tanmaysr019@gmail.com"
  target="_blank"
  class="block w-full text-center px-6 py-4
         bg-white text-black rounded-xl
         font-medium hover:bg-neutral-200 transition"
>
  Email Me
</a>
          <p class="mt-4 text-xs text-neutral-500 text-center">
            tanmaysr019@gmail.com
          </p>
        </div>

      </div>
    </div>

    <!-- 3D / GLOW ELEMENTS -->
    <div
      class="absolute top-1/4 -left-32 w-96 h-96
             bg-gradient-to-r from-indigo-500/20 to-purple-500/20
             rounded-full blur-3xl"
    ></div>

    <div
      class="absolute bottom-0 -right-32 w-96 h-96
             bg-gradient-to-r from-cyan-500/20 to-emerald-500/20
             rounded-full blur-3xl"
    ></div>
  </section>
</template>
