<script>

</script>

<template>
  <section>
    <div class="background-container">
      <img class="logo" src="../assets/icon-youtube-play.png" alt="">
    </div>
  </section>
</template>

<style scoped>
section {
  padding-top: 5rem;
}

.background-container {
  border-radius: 10px;
  margin: 0 auto;
  position: relative; 
  width: 900px; 
  height: 500px; 
  overflow: hidden; 
}

.background-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('../assets/artist-video-poster.jpg');
  background-size: cover; 
  background-position: center; 
  transition: transform 0.3s ease; 
}

.background-container:hover::before {
  transform: scale(1.1); 
}

.logo {
  position: absolute;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%); 
}
</style>