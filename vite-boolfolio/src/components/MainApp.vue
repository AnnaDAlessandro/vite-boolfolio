<script>
import axios from 'axios';

export default {
  name: 'MainApp',
 
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
  <main>
    <h2>Posto per stampare i Project</h2>
      <ul>
        <li v-for="(element,index) in arrayProjects"
        :key="element.id">{{ element.title }}</li>
      </ul>
   
  </main>
</template>

<style scoped>

</style>
