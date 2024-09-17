<template>
  <div class="section d-flex justify-content-center">
<!-- <ProjectsCard>
    <template #Project1></template>
    <template #Project2></template>
    <template #Project3></template>
    <template #Project4></template>
</ProjectsCard> -->

    <div class="projects-grid">
        <EduCard v-for="project in projects" :key="project.id">
                <template #BookCover>
        
                </template>
                <template #BookContent>
                    
                </template>
        
        </EduCard>
    </div>

    
</div>
</template>

<script setup>
import EduCard from  '@/components/EduCard.vue'
// import ProjectsCard from '@/components/ProjectsCard.vue'
import { useStore } from "vuex";
const store = useStore();
import {computed, onMounted} from  'vue';


const projects = computed(() => store.state.projects);

onMounted(() => {
    store.dispatch("fetchProjects");
  });

</script>
