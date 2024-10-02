<template>
  <Projects :projects="projects"/>
</template>

<script lang="ts">
import Header from '../components/Navigation.vue';
import ProjectList from '../components/Projects.vue';

definePageMeta({
  layout:'default'
})


interface Project {
  id: number;
  title: string;
  description: string;
  image: string;
}

export default {
  name: 'Portfolio',
  components: {
    Header,
    ProjectList,
  },
  data() {
    return {
      projects: [
        { id: 1, title: 'Project Nyomás', description: 'Megnyomtuk', image: 'path/to/image2.png' },
        { id: 2, title: 'Project One', description: 'A great project', image: 'path/to/image1.jpg' },
        { id: 3, title: 'Project Two', description: 'Another cool project', image: 'path/to/image2.jpg' },
        { id: 4, title: 'Project Three', description: 'Yet another project', image: 'path/to/image3.jpg' },
      ] as Project[],
    };
  },
};
</script>

<style scoped>
body {
  font-family: 'Inter', sans-serif;
}
</style>