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
        { name: 'Mina Hollace',role:'Freelance', src: img1, alt: 'High level of efficency and scientific teaching methods', text: 'I am free to learn on my own pace, follow my own schedule an choose the subject i want to learn from the syllabus,Great study portal for people like me' },
        { name: 'Mina Hollace',role:'Freelance', src: img2, alt: 'High level of efficency and scientific teaching methods', text: 'I am free to learn on my own pace, follow my own schedule an choose the subject i want to learn from the syllabus,Great study portal for people like me' },
        { name: 'Mina Hollace',role:'Freelance', src: img3, alt: 'High level of efficency and scientific teaching methods', text: 'I am free to learn on my own pace, follow my own schedule an choose the subject i want to learn from the syllabus,Great study portal for people like me' },
        { name: 'Mina Hollace',role:'Freelance', src: img4, alt: 'High level of efficency and scientific teaching methods', text: 'I am free to learn on my own pace, follow my own schedule an choose the subject i want to learn from the syllabus,Great study portal for people like me' }
      ]
    };
  }
};
</script>

<template>
 <section>
  <div class="mt-5 mb-5 text-center">
      <h2 class="melody">Testimonials</h2>
      <h2>Why do people love me?</h2>
    </div>
  <div class="container-fluid">
    <div class="carousel">
      <div v-for="(card, index) in images"
       :key="index" class="image-box" 
       :class="{ 'current': index === currentIndex,
       'adjacent': index === currentIndex - 1 || index === currentIndex + 1 || (currentIndex === 0 && index === images.length - 1)
       || (currentIndex === images.length - 1 && index === 0),
        }">
        <div class="text-container">
          <h3 class="card-title">{{ card.alt }}</h3>
          <p class="card-description"> {{ card.text }}</p>
        </div>
        <div class="img-container">
         <img :src="card.src" :alt="card.alt" class="avatar rounded-circle"/>
        </div>
        <span class="name"> {{ card.name }}</span>
        <span class="role">/{{ card.role }}</span>
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
</section>
</template>

<style scoped>
section{
  background-color: #F5F5F5;
  margin-top: 5rem;
  margin-bottom: 5rem;
  padding-bottom: 2rem;
}
.carousel {
  width: 100%;
  justify-content: space-around;
  margin: 0 auto;
  display: flex;
  flex-wrap: nowrap;
  
  overflow-x: auto;
}
.image-box.current{
  opacity: 1;
}
.image-box.adjacent{
  opacity: 0.5;
}
.image-box.hidden{
  display: none;
}
.image-box {
  background-color: #FFFFFF;
  overflow: hidden;
  width: calc(98vw / 3);
  height: 350px;
  text-align: left;
  position: relative;
  transition: opacity 0.3s;
  padding-left: 1.5rem;
  flex-shrink: 0;
}
.img-container {
  width: 70px;
  height: 70px;
  position: absolute;
  bottom: 20px;
  left: 20px;
}
.avatar {
  width: 100%;
  height: auto;
}
.image-box.inactive {
  opacity: 0.4;

}
.text-container {
  margin-bottom: 40px;
}
.card-title {
  font-size: 1.2em;
  margin: 10px 0;
}
.card-description {
  font-size: 1em;
  color: black;
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
  background-color: lightskyblue;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
  transition: background-color 0.3s;
}
.dot.active {
  background-color:black;
}
.role{
  position: absolute;
  bottom: 20px;
  left:105px;
  color: gray;
}
.name{
  position: absolute;
  bottom: 45px;
  left: 105px;
}
</style>