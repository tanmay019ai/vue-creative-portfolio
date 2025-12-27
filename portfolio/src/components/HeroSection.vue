<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue"
import profile from "@/assets/profile.jpg"

/* =========================
   TYPEWRITER ROLES
========================= */
const roles = [
  { text: "Web Developer", color: "text-white" },
  { text: "App Developer", color: "text-neutral-300" },
  { text: "Freelancer", color: "text-yellow-300" },
  { text: "Agentic System Builder", color: "text-violet-300" },
  { text: "RAG System Engineer", color: "text-indigo-300" },
  { text: "ML Automation Engineer", color: "text-cyan-300" },
  { text: "Logo & Digital Content Creator", color: "text-emerald-300" },
]

const currentText = ref("")
const currentColor = ref("text-white")
let roleIndex = 0
let charIndex = 0
let isDeleting = false

const typeEffect = () => {
  const role = roles[roleIndex]

  if (!isDeleting) {
    currentText.value = role.text.slice(0, ++charIndex)
    currentColor.value = role.color
    if (charIndex === role.text.length) {
      setTimeout(() => (isDeleting = true), 1200)
    }
  } else {
    currentText.value = role.text.slice(0, --charIndex)
    if (charIndex === 0) {
      isDeleting = false
      roleIndex = (roleIndex + 1) % roles.length
    }
  }

  setTimeout(typeEffect, isDeleting ? 40 : 80)
}

/* =========================
   SCROLL PARALLAX
========================= */
const scrollY = ref(0)
const onScroll = () => (scrollY.value = window.scrollY)

onMounted(() => {
  typeEffect()
  window.addEventListener("scroll", onScroll)
})
onUnmounted(() => window.removeEventListener("scroll", onScroll))
</script>

<template>
  <section
    class="relative min-h-screen bg-black text-white overflow-hidden
           flex items-center justify-center px-4 sm:px-6"
  >
    <!-- BACKGROUND BLOBS (NON-CLICKABLE) -->
    <div
      class="blob left bg-gradient-to-r from-indigo-600/40 to-violet-600/40"
      :style="{ transform: `translateX(${scrollY * 0.15}px)` }"
    ></div>

    <div
      class="blob right bg-gradient-to-r from-cyan-500/30 to-emerald-500/30"
      :style="{ transform: `translateX(-${scrollY * 0.12}px)` }"
    ></div>

    <!-- MAIN GRID -->
    <div
      class="relative z-10 max-w-6xl w-full
             grid grid-cols-1 md:grid-cols-2
             gap-12 items-center"
    >
      <!-- IMAGE FIRST ON MOBILE -->
      <div
        class="relative flex justify-center md:justify-end perspective
               order-1 md:order-2"
      >
        <div class="ring hidden sm:block"></div>

        <div class="photo-card">
          <img :src="profile" alt="Profile" />
        </div>
      </div>

      <!-- TEXT -->
      <div
        class="text-center md:text-left
               order-2 md:order-1
               transition-all duration-300"
        :style="{
          transform: `translateY(-${scrollY * 0.15}px)`,
          opacity: `${1 - scrollY / 700}`
        }"
      >
        <!-- TITLE -->
        <h1
          class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl
                 font-semibold tracking-tight leading-tight"
        >
          I am a
          <span
            :class="[
              'ml-2 border-r-2 border-white/40 pr-1 whitespace-nowrap',
              currentColor
            ]"
          >
            {{ currentText }}
          </span>
        </h1>

        <!-- IDENTITY LINE -->
        <p
          class="mt-6 text-sm sm:text-base
                 text-neutral-400 tracking-wide"
        >
          Freelancer · YouTuber · Content Creator · B.Tech Student · Software Engineer
        </p>

        <!-- CTA -->
        <div
          class="mt-8 flex flex-col sm:flex-row
                 gap-4 justify-center md:justify-start"
        >
          <!-- VIEW WORK (FIXED) -->
         <a
  href="#featured-work"
  class="relative z-20 inline-flex items-center justify-center
         px-8 py-3 bg-white text-black rounded-lg
         font-medium hover:bg-neutral-200 transition"
>
  View Work
</a>


          <button
            class="relative z-20 px-8 py-3 border border-white/20 rounded-lg
                   hover:bg-white/5 transition"
          >
            Contact
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* ===== BACKGROUND BLOBS ===== */
.blob {
  position: absolute;
  width: 420px;
  height: 420px;
  filter: blur(140px);
  border-radius: 9999px;
  pointer-events: none; /* 🔑 FIX */
}
.blob.left {
  top: 25%;
  left: -15%;
}
.blob.right {
  top: 10%;
  right: -15%;
}

/* ===== 3D IMAGE ===== */
.perspective {
  perspective: 1200px;
}

.photo-card {
  width: 220px;
  height: 300px;
  border-radius: 20px;
  overflow: hidden;
  background: rgba(255, 255, 255, 0.08);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.15);
  transform: rotateY(-10deg) rotateX(6deg);
  animation: float 6s ease-in-out infinite;
  z-index: 2;
}

@media (min-width: 768px) {
  .photo-card {
    width: 280px;
    height: 360px;
  }
}

.photo-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* ===== RING ===== */
.ring {
  position: absolute;
  width: 340px;
  height: 340px;
  border-radius: 50%;
  border: 1px solid rgba(255, 255, 255, 0.2);
  animation: spin 18s linear infinite;
  transform: rotateX(70deg);
  pointer-events: none; /* 🔑 FIX */
}

/* ===== ANIMATIONS ===== */
@keyframes float {
  0%, 100% {
    transform: rotateY(-10deg) rotateX(6deg) translateY(0);
  }
  50% {
    transform: rotateY(-10deg) rotateX(6deg) translateY(-14px);
  }
}

@keyframes spin {
  from {
    transform: rotateX(70deg) rotateZ(0deg);
  }
  to {
    transform: rotateX(70deg) rotateZ(360deg);
  }
}
</style>
