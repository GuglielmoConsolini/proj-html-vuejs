<script>
import SezioneCards from '../components/SezioneCards.vue';
import SezioneGetStarted from '../components/SezioneGetStarted.vue';
import SezioneYoutube from '../components/SezioneYoutube.vue';
import SezioneSlider from '../components/SezioneSlider.vue';
import AppCoursesShop from '../components/AppCoursesShop.vue';
import SezioneBlog from '../components/SezioneBlog.vue';
export default {

components: {
  SezioneCards,
  SezioneGetStarted,
  SezioneYoutube,
  SezioneSlider,
  AppCoursesShop,
  SezioneBlog,
},
data() {
  return {
    
  }
},
methods: {
  

},
mounted() {
  
}
}

</script>

<template>
  <div class="transition1"></div>
  <SezioneCards/>
  <SezioneGetStarted/>
  <SezioneYoutube/>
  <div class="transition2"></div>
  <SezioneSlider/>
  <AppCoursesShop/>
  <SezioneBlog/>
</template>

<style scoped>
  .transition1{
    height: 50px;
    background: linear-gradient(to bottom,  #FBF9F6,white);
  }
  .transition2 {
    height: 50px;
    background: linear-gradient(to bottom, white, #F5F5F5);
  }
  .index{
    z-index: 999;
  }
</style>