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
  <div class="container-fluid ps-5 mb-5">
    <div class="shape5">
      <img src="../assets/artist-shape-02-600x324.png" alt="">
    </div>
    <div class="shape4">
      <img src="../assets/maxcoach-shape-05-150x150.png" alt="">
    </div>
    <div class="shape3">
      <img src="../assets/maxcoach-shape-14-1536x343.png" alt="">
    </div>
    <div class="shape2">
      <img src="../assets/artist-shape-01.png" alt="">
    </div>
    <div class="mt-5 text-center">
      <h2 class="melody">Artist Coaching</h2>
      <h2>I understand what it takes to create.<br>I can help you with</h2>
    </div>
    <section class="card-section">
      <div class="shape1">
       <img src="../assets/maxcoach-shape-13-150x150.png" alt="">
    </div>
      <Card v-for="(card, index) in cards" :key="index" :image="card.image" :title="card.title" :description="card.description"/>
    </section>
  </div>
</template>
  
  <style>
  .shape1{
    position: absolute;
    right: -115px;
    top: -100px;
    z-index: 10;
  }
  .shape2{
    position: absolute;
    transform: rotate(220deg);
    left: -100px;
    top: 40px;
    z-index: 10;
  }
  .shape3{
    position: absolute;
    z-index: 3;
    left: 0;
  }
  .shape4{
    position: absolute;
    bottom: 0;
  }
  .shape5{
    position: absolute;
    top: -40px;
    right: -250px;
    transform: rotate(40deg);
  }
  .melody {
    color: #6AC5f1;
    font-size: 50px;
    font-family: myFirstFont;
  }
  @font-face {
    font-family: myFirstFont;
    src: url(/public/Rossela-Demo.ttf);
  }
  .card-section {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
    padding: 10px;
    position: relative;
    
    width: 90%;
    margin: auto;
    margin-top: 8rem;
  }
  </style>