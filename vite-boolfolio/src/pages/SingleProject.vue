
<script>
import axios from 'axios';
export default {
  name: 'SingleProject',
 
  data() {
    return {
        project:null    
    };
  },
  methods:{
    getSingleProject(){
        axios.get(`http://127.0.0.1:8000/api/test/${this.$route.params.slug}`)
         .then(res =>{
            if(res.data.success){
                this.project = res.data.project
            }else{
               
            }
         })
    }
  },
  mounted(){
     this.getSingleProject()
  }
};
</script>
   



<template>
   <h3 v-if="project">{{ project.title }}</h3>
    <p v-if="project">{{ project.content }}</p>
</template>
  
  
  <style scoped >
  
  
  </style>