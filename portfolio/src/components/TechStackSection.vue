<script setup lang="ts">
/* ===== SVG IMPORTS (ONLY WHAT YOU HAVE) ===== */
import html from "@/assets/techstack/HTML5.svg";
import css from "@/assets/techstack/CSS3.svg";
import js from "@/assets/techstack/JavaScript.svg";
import react from "@/assets/techstack/React.svg";
import vue from "@/assets/techstack/Vue.svg";

import node from "@/assets/techstack/Node.js.svg";
import python from "@/assets/techstack/Python.svg";
import django from "@/assets/techstack/Django.svg";
import flask from "@/assets/techstack/Flask.svg";

import expo from "@/assets/techstack/expo.svg";
import android from "@/assets/techstack/Android.svg";

import tensorflow from "@/assets/techstack/TensorFlow.svg";
import pytorch from "@/assets/techstack/PyTorch.svg";
import sklearn from "@/assets/techstack/scikit-learn.svg";
import pandas from "@/assets/techstack/Pandas.svg";
import numpy from "@/assets/techstack/NumPy.svg";

import langchain from "@/assets/techstack/langchain.svg";
import openai from "@/assets/techstack/OpenAPI.svg";

import mongodb from "@/assets/techstack/MongoDB.svg";
import mysql from "@/assets/techstack/MySQL.svg";
import postgresql from "@/assets/techstack/PostgresSQL.svg";
import redis from "@/assets/techstack/Redis.svg";

import figma from "@/assets/techstack/Figma.svg";
import photoshop from "@/assets/techstack/Adobe Photoshop.svg";
import illustrator from "@/assets/techstack/Adobe Illustrator.svg";

import git from "@/assets/techstack/Git.svg";
import docker from "@/assets/techstack/Docker.svg";
import vercel from "@/assets/techstack/Vercel.svg";
import linux from "@/assets/techstack/Linux.svg";

/* ===== TECH STACK DATA ===== */
const stacks = [
  {
    title: "Frontend",
    items: [
      { name: "HTML", icon: html },
      { name: "CSS", icon: css },
      { name: "JavaScript", icon: js },
      { name: "React", icon: react },
      { name: "Vue", icon: vue },
    ],
  },
  {
    title: "Backend",
    items: [
      { name: "Node.js", icon: node },
      { name: "Python", icon: python },
      { name: "Django", icon: django },
      { name: "Flask", icon: flask },
      { name: "REST APIs", emoji: "🔌" },
      { name: "JWT Auth", emoji: "🔐" },
    ],
  },
  {
    title: "App Development",
    items: [
      { name: "React Native", emoji: "📱" },
      { name: "Expo", icon: expo },
      { name: "Android", icon: android },
      { name: "Mobile UI", emoji: "🎨" },
    ],
  },
  {
    title: "AI / ML",
    items: [
      { name: "TensorFlow", icon: tensorflow },
      { name: "PyTorch", icon: pytorch },
      { name: "Scikit-learn", icon: sklearn },
      { name: "Pandas", icon: pandas },
      { name: "NumPy", icon: numpy },
    ],
  },
  {
    title: "Agentic AI & RAG",
    items: [
      { name: "LangChain", icon: langchain },
      { name: "OpenAI API", icon: openai },
      { name: "RAG Pipelines", emoji: "🧠" },
      { name: "Vector Databases", emoji: "🗂️" },
      { name: "LLM Integration", emoji: "🤖" },
    ],
  },
  {
    title: "Database",
    items: [
      { name: "MongoDB", icon: mongodb },
      { name: "MySQL", icon: mysql },
      { name: "PostgreSQL", icon: postgresql },
      { name: "Redis", icon: redis },
      { name: "DB Design", emoji: "📊" },
    ],
  },
  {
    title: "Graphic / Content",
    items: [
      { name: "Figma", icon: figma },
      { name: "Photoshop", icon: photoshop },
      { name: "Illustrator", icon: illustrator },
      { name: "Content Creation", emoji: "🎥" },
      { name: "Logo Design", emoji: "🖌️" },
    ],
  },
  {
    title: "Tools & Platforms",
    items: [
      { name: "Git", icon: git },
      { name: "Docker", icon: docker },
      { name: "Vercel", icon: vercel },
      { name: "Linux", icon: linux },
      { name: "Postman", emoji: "📮" },
    ],
  },
];
</script>

<template>
  <section  id="tech-stack" class="bg-black text-white py-28 px-4 sm:px-6">
    <div class="max-w-7xl mx-auto">

      <!-- TITLE -->
      <h2 class="text-4xl font-semibold text-center">
        Tech Stack
      </h2>

      <p class="mt-4 text-neutral-400 text-center max-w-3xl mx-auto">
        Technologies and systems I work with across frontend, backend, AI, and product development.
      </p>

      <!-- GRID -->
      <div class="mt-16 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
        <div
          v-for="(stack, i) in stacks"
          :key="i"
          class="bg-white/5 border border-white/10 rounded-2xl p-6 backdrop-blur
                 hover:border-white/20 transition"
        >
          <h3 class="text-lg font-medium mb-4">
            {{ stack.title }}
          </h3>

          <ul class="space-y-3 text-sm text-neutral-300">
            <li
              v-for="(item, j) in stack.items"
              :key="j"
              class="flex items-center gap-3"
            >
              <img
                v-if="item.icon"
                :src="item.icon"
                :alt="item.name"
                class="w-5 h-5 object-contain"
              />
              <span v-else class="text-lg">
                {{ item.emoji }}
              </span>
              <span>{{ item.name }}</span>
            </li>
          </ul>
        </div>
      </div>

    </div>
  </section>
</template>
