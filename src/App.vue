<template>
<Navbar/>
  <router-view/>
</template>

<script>
import Navbar from '@/components/NavbarView.vue'
export default {
  components: { Navbar }
}


</script>

<style src="./assets/css/style.css">
</style>
