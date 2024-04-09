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
    <h3>Progetto:</h3>
    <div class="card-container">
        <div class="card-body">
          <h5 class="card-title">{{ project.title }}</h5>
          <p class="card-text">{{ project.content }}</p>
          <a href="#" class="btn btn-primary">Vai da qualche parte</a>
        </div>
      </div>
    </div>

  </main>
</template>
  
  
  <style scoped >
  .project-card {
  margin-bottom: 20px; /* Aggiungi spazio sotto la sezione */
}

.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between; /* Distribuisci gli spazi tra le card */
}

.card {
  width: calc(25% - 10px); /* Imposta la larghezza di ogni card al 25% del contenitore meno lo spazio tra le card */
  margin-bottom: 20px; /* Aggiungi spazio tra le card */
}

.card-body {
  text-align: center; 
}

  
  </style>
  