<script>
import SezioneCards from './components/SezioneCards.vue';
import SezioneGetStarted from './components/SezioneGetStarted.vue';
import SezioneYoutube from './components/SezioneYoutube.vue';
import SezioneSlider from './components/SezioneSlider.vue';
import AppHeader from './components/AppHeader.vue';
import AppCoursesShop from './components/AppCoursesShop.vue';
export default {

  components: {
    SezioneCards,
    SezioneGetStarted,
    SezioneYoutube,
    SezioneSlider,
    AppHeader,
    AppCoursesShop,
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
  <AppHeader />
  <SezioneCards />
  <SezioneGetStarted />
  <SezioneYoutube />
  <SezioneSlider />
  <AppCoursesShop />
    
</template>

<style>
  
</style>