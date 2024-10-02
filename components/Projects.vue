<template>
  <section class="flex gap-6">
    <div v-for="project in projects" :key="project.id" class="w-[340px] h-[240px] bg-white/10 backdrop-blur-md p-6 rounded-lg border border-white/20 hover:shadow-2xl transition-shadow">
      <img :src="project.image" alt="project image" class="rounded-md mb-4" />
      <h3 class="text-xl font-semibold text-white mb-2">{{ project.title }}</h3>
      <p class="text-white/80">{{ project.description }}</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface Project {
  id: number;
  title: string;
  description: string;
  image: string;
}

export default defineComponent({
  name: 'ProjectList',
  props: {
    projects: {
      type: Array as () => Project[],
      required: true,
    },
  },
});
</script>