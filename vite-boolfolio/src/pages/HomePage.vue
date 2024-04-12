<script>
import axios from 'axios';
import ProjectCard from '../components/ProjectCard.vue';


export default {
  name: 'HomePage',
  components: {
    ProjectCard
    
   },
 
  data() {
    return {
        arrayProjects: []
    }
  },
  methods: {
    getProjects() {
      axios.get('http://127.0.0.1:8000/api/test')
        .then(res => {
          console.log(res.data.projects);
          this.arrayProjects = res.data.projects;
        })
        
    }
        
    },
  
  mounted() {
    this.getProjects();
  }
}   
</script>


<template>
  <h1  class="text-center my-5">Qui troverai tutti i Progetti:</h1>

  <ProjectCard v-for="(element,index) in arrayProjects" 
  :key="element.id"
  :title="element.title"
  :content="element.content"
  :slug="element.slug"
  :category="element.category ? element.category.name : ''"
  :technologies="element.technologies"/>

  <!--<ul  class="text-center list-unstyled my-5">
    <li v-for="(element,index) in arrayProjects" :key="element.id">
        <router-link :to="{name:'single-project', params:{slug:element.slug}}">
            {{ element.title }}
        </router-link>
    </li>
  </ul> -->
  
</template>

<style scoped>

</style>
