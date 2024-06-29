<script setup>
import Star from "./icons/Star.vue"

const props = defineProps(["film"]);
const imgSrc = props.film.img;
const rating = props.film.rating;
</script>

<template>
  <div class="wrapper">
    <div class="img-box">
      <img :src="imgSrc" alt="poster" />
    </div>
    <div class="detail-box">
      <h3 class="title">{{ props.film.title }}</h3>
      <p class="descr">{{ props.film.description }}</p>
      <div class="rating">Rating({{ rating }}/5): 
        <Star v-for="n in rating"></Star>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  min-width: 250px;
  border: 1px solid #bababa84;
  background-color: #ffffff65;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  box-shadow: 2px 2px 5px #0000003c;
}

.img-box {
  width: 100%;
  height: 70%;
  overflow: hidden;
}

img {
  width: 100%;
}

.detail-box{
    font-family: "Jost", sans-serif;
    display: flex;
    flex-direction: column;
    justify-content: start;
    flex-grow: 1;
    padding: 10px;
}

.title{
    font-weight: 700;
    margin: 10px 0;
}

.descr{
    /* margin: 10px 0; */
    flex-grow: 1;
}

.rating{
    display: flex;
    align-items: center;
    gap: 10px;
}

</style>
