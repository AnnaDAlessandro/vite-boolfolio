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
   



   <template>
  <main>
    <div class="project-card">
      <h3>Progetto:</h3>
    
    </div>
    <div class="card" style="width: 18rem;">
      <div class="card-body">
        <h5>{{ project.title }}</h5>
        <p>{{ project.content }}</p>
        <a href="#" class="btn btn-primary">Vai da qualche parte</a>
      </div>
    </div>
  </main>
</template>
  </template>
  
  <style scoped>
  
  </style>
  