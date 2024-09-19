<template>
<div class="section d-flex justify-content-center">
  <div class="projects-grid">
    <div v-for="project in projects" :key="project.id" class="col-12 col-sm-6 col-md-4 col-lg-3 mb-4">
      <Card class="card h-100">
        <template #CardHeader>
          <img :src="project.img_url" alt="projects" loading="lazy" class="card-img-top">
        </template>

        <template #CardBody>
          <div class="card-body">
            <h3 class="card-title">{{ project.projectTitle }}</h3>
            <p class="card-text">{{ project.description }}</p>

            <div class="btns d-flex justify-content-evenly">
              <a :href="project.vercel_link" target="_blank">
                <i class="bi bi-broadcast"></i>
              </a>

              <a :href="project.gitHub_link" class="button" target="_blank">
                <i class="bi bi-github"></i>
              </a>
            </div>
          </div>
        </template>
      </Card>
    </div>
  </div>
</div>




</template>

<script setup>
import Card from  '@/components/Card.vue'
// import ProjectsCard from '@/components/ProjectsCard.vue'
import { useStore } from "vuex";
const store = useStore();
import {computed, onMounted} from  'vue';


const projects = computed(() => store.state.projects);

onMounted(() => {
    store.dispatch("fetchProjects");
  });

</script>

<style scoped>

.row{
  margin: 0;
  padding: 0;
  justify-content: center;
}

.card img{
  width: 100%;
  height: 15rem;
  object-fit: contain;
  border-radius: 10px;
}


.card:hover{
background-color: tan;

}
  .button {

  align-items: center;
  gap: 15px;
  outline-offset: -3px;
  cursor: pointer;
  transition: 400ms;
  width: 50%;
}

  /* Media queries */
  @media screen and (width > 800px){
    Card{
     flex-direction: column;
      
    }
  }

</style>
