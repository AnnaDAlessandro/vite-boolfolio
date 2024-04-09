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
            
    };
  }
};
</script>

<template>
   
    <main>
    <div class="project-card">
      <h3>Progetti:</h3>
    <ul>
      <li v-for="(project, index) in project" :key="index">
        {{ project.title }}
      </li>
      <li v-for="(project, index) in project" :key="index">
        {{ project.content }}
      </li>
    </ul>
    </div>
    </main>
  </template>
  
  <style scoped>
  
  </style>
  