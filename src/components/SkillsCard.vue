<template>
<div class="flip-card">
    <div class="flip-card-inner">
        <div class="flip-card-front">
            <slot name="CardFront"></slot>
        </div>
        <div class="flip-card-back">
            <slot name="CardBack"></slot>
        </div>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>
/* .flip-card {
  width: 190px;
  height: 254px;
  perspective: 1000px;
  font-family: sans-serif;
} */

/* .flip-card-front,
.flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
} */

.flip-card {
  width: 300px;
  height: 200px;
  border: none;
  perspective: 1000px;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d; 
}

.title {
  font-size: 1.5em;
  font-weight: 900;
  text-align: center;
  margin: 0;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  box-shadow: 0 8px 14px 0 rgba(0,0,0,0.2);
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  /* border: 1px solid #A27035; */
  border-radius: 1rem;
}

.flip-card-front {
  background-color: #FFE0B5;
  border: 1px solid  #A27035;

}

.flip-card-back {
     background-color: #A27035;
     border: 1px solid  bisque;


  color: white;
  transform: rotateY(180deg);
}


</style>