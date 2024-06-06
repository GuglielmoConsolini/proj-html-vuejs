<script>
import SezioneCards from './components/SezioneCards.vue';
import SezioneGetStarted from './components/SezioneGetStarted.vue';
import SezioneYoutube from './components/SezioneYoutube.vue';
import SezioneSlider from './components/SezioneSlider.vue';
import AppHeader from './components/AppHeader.vue';
import AppCoursesShop from './components/AppCoursesShop.vue';
import SezioneBlog from './components/SezioneBlog.vue';
import AppFooter from './components/AppFooter.vue';
export default {

  components: {
    SezioneCards,
    SezioneGetStarted,
    SezioneYoutube,
    SezioneSlider,
    AppHeader,
    AppCoursesShop,
    SezioneBlog,
    AppFooter,
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
  <div class="transition1"></div>
  <SezioneCards />
  <SezioneGetStarted />
  <SezioneYoutube />
  <div class="transition2"></div>
  <SezioneSlider />
  <AppCoursesShop />
  <SezioneBlog />
  <AppFooter />
    
</template>

<style>
  .transition1{
    height: 50px;
    background: linear-gradient(to bottom, #FBF9F6,white);
  }
  .transition2 {
    height: 50px;
    background: linear-gradient(to bottom, white, #F5F5F5);
  }
  .index{
    z-index: 999;
  }
</style>