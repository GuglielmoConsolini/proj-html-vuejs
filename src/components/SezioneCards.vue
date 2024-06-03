<script>
  import Card from './Card.vue'
  import image1 from '../assets/artist-box-image-01.png'
  import image2 from '../assets/artist-box-image-02.png'
  import image3 from '../assets/artist-box-image-03.png'
  import image4 from '../assets/artist-box-image-04.png'
  
  export default {
    components: {
      Card,
    },
    data() {
      return {
        cards: [
          { image: image1, title: 'Online Courses', description: 'Online art coaching now offers you a very powerful way to redesign your artist mind.' },
          { image: image2, title: 'One to One', description: 'Getting the necessary clarity about the current state to help you improve your ability.' },
          { image: image3, title: 'Anywhere', description: 'Access to valuable and portable program which allow you to setup and live anywhere you want.' },
          { image: image4, title: 'Ontime', description: 'Punctuality is our top priority because its an essential criteria to assess a program quality.' }
        ]
      }
    }
  }
  </script>

<template>
  <div class="container-fluid">
    <img class="position-absolute top-50 start-100 translate-middle" src="../assets/maxcoach-shape-13-150x150.png" alt="">
    <div class="mt-5 text-center">
      <h2 class="melody">Artist Coaching</h2>
      <h2>I understand what it takes to create.<br>I can help you with</h2>
    </div>
    <section class="card-section mt-5">
      <Card v-for="(card, index) in cards" :key="index" :image="card.image" :title="card.title" :description="card.description"/>
    </section>
  </div>
</template>
  
  <style>
  .melody {
    color: #1972F5;
    font-size: 40px;
  }
  
  .card-section {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
    padding: 10px;
  }
  </style>