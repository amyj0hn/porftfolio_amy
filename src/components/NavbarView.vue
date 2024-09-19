<template>
<div class="side-nav">
  <button class="navbar-toggler" d-md-none type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"><i class="bi bi-list"></i></span>
  </button>

  <div class="collapse d-md-block navbar-collapse" id="navbarNav">
    <ul class="nav flex-column">
      <li class="nav-item">
        <router-link class="nav-link active" aria-current="page" to="/">Home</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/about">About</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/education">Education</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/projects">Projects</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/contact">Contact</router-link>
      </li>
    </ul>
  </div>
</div>

</template>

<script>
export default {

}
</script>

<style scoped>
.side-nav {
  position: fixed; 
  left: 0; 
  top: 0; 
  height: 100vh;
  width: 200px; 
  background-color: #533E2D; 
  padding: 20px;
}
.nav {
  display: flex;
}

.nav-link{
  color:  #D8AE7E;
}

.nav-link.active{
  font-weight: bold;
}

.navbar-toggler{
  color: aliceblue;
}

</style>