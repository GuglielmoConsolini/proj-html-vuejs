<script>
import SezioneCards from './components/SezioneCards.vue';
import SezioneGetStarted from './components/SezioneGetStarted.vue';
import SezioneYoutube from './components/SezioneYoutube.vue';
import SezioneSlider from './components/SezioneSlider.vue';
export default {

  components: {
    SezioneCards,
    SezioneGetStarted,
    SezioneYoutube,
    SezioneSlider,
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
    <Main>
      <SezioneCards />
      <SezioneGetStarted />
      <SezioneYoutube />
      <SezioneSlider />
    </Main>
</template>

<style>
  
</style>