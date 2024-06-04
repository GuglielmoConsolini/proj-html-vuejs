<script>
import img1 from '../assets/artist-testimonial-avatar-01.jpg';
import img2 from '../assets/artist-testimonial-avatar-02.jpg';
import img3 from '../assets/artist-testimonial-avatar-03.jpg';
import img4 from '../assets/artist-testimonial-avatar-04.jpg';

export default {
  name: 'Carousel',
  data() {
    return {
      currentIndex: 1,
      images: [
        { src: img1, alt: 'Artist 1' },
        { src: img2, alt: 'Artist 2' },
        { src: img3, alt: 'Artist 3' },
        { src: img4, alt: 'Artist 4' }
      ]
    };
  }
};
</script>

<template>
  <div class="mt-5 mb-5 text-center">
      <h2 class="melody">Testimonials</h2>
      <h2>Why do people love me?</h2>
    </div>
  <div class="container-fluid">
    <div class="carousel">
      <div v-for="(card, index) in images" :key="index" class="card" :class="{ 'inactive': index !== currentIndex }">
        <img :src="card.src" :alt="card.alt" class="card-image rounded-circle"/>
        <h3 class="card-title">{{ card.alt }}</h3>
        <p class="card-description">Description for {{ card.alt }}</p>
      </div>
    </div>
    <div class="navigation-dots">
      <span
        v-for="(dot, index) in images" 
        :key="index" 
        class="dot" 
        :class="{ 'active': index === currentIndex }"
        @click="currentIndex = index"
      ></span>
    </div>
  </div>
</template>

<style scoped>
.carousel {
  width: 80%;
  justify-content: space-between;
  margin: 0 auto;
  display: flex;
  gap: 20px;
}
.card {
  border-radius: 8px;
  overflow: hidden;
  width: 200px;
  text-align: center;
  transition: opacity 0.3s;
}
.card.inactive {
  opacity: 0.4;
}
.card-image {
  width: 100%;
  height: auto;
}
.card-title {
  font-size: 1.2em;
  margin: 10px 0;
}
.card-description {
  font-size: 1em;
  color: black;
  padding: 0 10px 10px;
}
.navigation-dots {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}
.dot {
  height: 15px;
  width: 15px;
  margin: 0 5px;
  background-color: gray;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
  transition: background-color 0.3s;
}
.dot.active {
  background-color:black;
}
</style>