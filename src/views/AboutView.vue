<template>
  <!-- <div class="section">
    <div class="row">
    <div class="col">
      <div id="details" data-aos="fade-right" data-aos-duration="3000">
        <h3 class="display-5">So, Who is Amy?</h3>
        <p v-if="aboutMe?.length">
          <span>{{ aboutMe[0]?.description }}</span>
        </p>
        <Spinner v-else />
      </div>
    </div>
  </div>
<SkillsCard v-for="skill in skills" :key="skill.id" class="flip-card col-md-4 mb-4 ">
  <template #CardFront>
    <img :src="skill.img_url" alt="skills" loading="lazy" />

  </template>
  <template #CardBack>
    <h2>{{ skill.skill }}</h2>
    <p class="lead">{{ skill.description }}</p>
  </template>

</SkillsCard>
  </div> -->

  <div class="section">
  <div class="row">
    <div class="col">
      <div id="details" data-aos="fade-right" data-aos-duration="3000">
        <h3 class="display-5">So, Who is Amy?</h3>
        <p v-if="aboutMe?.length" class="desc">
          <span>{{ aboutMe[0]?.description }}</span>
        </p>
        <Spinner v-else />
      </div>
    </div>
  </div>

  <div class="row">
    <SkillsCard
      v-for="skill in skills"
      :key="skill.id"
      class="flip-card col-12 col-md-4 mb-4"
    >
      <template #CardFront>
        <img
          :src="skill.img_url"
          alt="skills"
          class="card-img-top"
          loading="lazy"
          style=" width: 100%; height: 100%;"
        />
      </template>
      <template #CardBack>
        <div class="card-body">
          <h2>{{ skill.skill }}</h2>
          <p class="lead">{{ skill.description }}</p>
        </div>
      </template>
    </SkillsCard>
  </div>
</div>

</template>

<script setup>
import SkillsCard from '@/components/SkillsCard.vue'
import Spinner from "@/components/SpinnerCOmp.vue";
import { computed, onMounted } from "vue";
import { useStore } from "vuex";

const store = useStore();

const skills = computed(() => store.state.skills);
const aboutMe = computed(() => store.state.aboutMe);



onMounted(()=>{
  store.dispatch("fetchSkills"),
  store.dispatch("fetchAbout")
})
</script>

<style scoped>
.lead{
 font-size: 13px;
 padding-left: 12px;
 text-align: center;
}

.row{
    margin: 0;
    padding: 0;
    justify-content: center;
  }

  .desc{
    font-size: 16px;
    margin: 3rem;
  }
</style>

