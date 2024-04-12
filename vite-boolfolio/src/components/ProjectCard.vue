<script>
export default {
  name: 'ProjectCard',
  props:
    [
    'title',
    'content',
    'slug',
    'category',
    'technologies'
  ],
  data() {
    return {
            
    };
  },
  methods:{
    
  },
  mounted(){

  }
};
</script>
   



<template>

  <router-link :to="{ name: 'single-project', params: { slug:slug } }">
    <div class="container">

    
    <div class="card my-5" style="width: 18rem;">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{ title }}</h5>
        <p class="card-text">{{ content }}</p>
        <p>Categoria:{{ category }}</p>
        <span v-for="(element,index) in technologies" :key="index">Tecnologia Utilizzata:{{ element.name }}</span>
      </div>
    </div>
  </div>

  </router-link>
</template>
  
  
  <style scoped >
  
  
  </style>
  