<template>
  <div class="section">
    <div class="row vh-100 align-items-center">
    <div class="col">
      <img
        src="https://amyj0hn.github.io/project-images/images/20240422_091901.jpg"
        alt="portfolio-picture"
        class="img-fluid w-75 shadow rounded-top"
      />
    </div>

    <div class="col">
      <div id="details">
        <div class="animate__animated animate__bounce">
          <h1 class="display-1" data-aos="fade-left"
     data-aos-easing="linear"
     data-aos-duration="1500">Amy Johnson</h1>
        </div>

        <p v-if="jobTitle?.length">
          I am a
          <span>{{ jobTitle[0]?.title }}</span>
        </p>
        <Spinner v-else />
      </div>
      <button type="button" class="btn"><router-link to="/contact" class="reachme">Reach Me</router-link></button>
    </div>
  </div>
  </div>

</template>

<script>

export default {
  name: 'HomeView',

}
</script>

<style scoped>
.color{
  background-color: #413620;
  color: aliceblue;
}

.btn {
 width: 6.5em;
 height: 2.3em;
 margin: 0.5em;
 background: tan;
 color: white;
 border: none;
 border-radius: 0.625em;
 font-size: 20px;
 font-weight: bold;
 cursor: pointer;
 position: relative;
 z-index: 1;
 overflow: hidden;
}

button:hover {
 color: tan;
}

button:after {
 content: "";
 background: white;
 position: absolute;
 z-index: -1;
 left: -20%;
 right: -20%;
 top: 0;
 bottom: 0;
 transform: skewX(-45deg) scale(0, 1);
 transition: all 0.5s;
}

button:hover:after {
 transform: skewX(-45deg) scale(1, 1);
 -webkit-transition: all 0.5s;
 transition: all 0.5s;
}

.reachme{
  text-decoration: none;
}
</style>
