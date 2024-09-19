<template>
  <div class="section">
    <EduCard v-for=" edu in education" :key="edu.id">
        <template #BookCover>
          <h3>{{edu.school}}</h3>
        </template>
        <template #BookContent>
            <p>{{ edu.year }}
              {{ edu.grade }}
            </p>
            <p class="lead">{{ edu.subjects.toString() }}</p>

        </template>
    </EduCard>

  </div>
</template>

<script setup>
import  EduCard from '@/components/EduCard.vue'

import { computed, onMounted } from "vue";
import { useStore } from "vuex";
const store = useStore();

const experience = computed(() => store.state.experience);
const education = computed(() => store.state.education);

onMounted(() => {
  store.dispatch("fetchExperience");
  store.dispatch("fetchEducation");
  console.log(experience);
  console.log(education);


});
</script>

