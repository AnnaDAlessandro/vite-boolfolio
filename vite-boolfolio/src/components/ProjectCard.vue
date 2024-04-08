<script>
export default {
  name: 'ProjectCard',
  props: {
    project: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      // Dati del componente
    };
  }
};
</script>

<template>
   
    <main>
    <div class="project-card">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </div>
    </main>
  </template>
  
  <style scoped>
  
  </style>
  