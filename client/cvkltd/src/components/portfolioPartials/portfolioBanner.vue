<template>
  <div class="portfolio-banner" :style="backgroundImageStyle">
    <div class="overlay"></div>
    <h1>Projects</h1>
  </div>
</template>

<script>
import backgroundImage from '@/assets/excavator.jpg';

export default {
  name: 'PortfolioBanner',
  data() {
    return {
      backgroundImage
    };
  },
  computed: {
    backgroundImageStyle() {
      return {
        backgroundImage: `url(${this.backgroundImage})`,
        backgroundSize: 'cover',
        backgroundPosition: 'center',
        width: '100%',
        height: '350px' 
      };
    }
  }
};
</script>

<style scoped>
.portfolio-banner {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(128, 128, 232, 0.5); /* Blue overlay with 50% opacity */
  z-index: 1;
}

h1 {
   position: absolute;
  /* align-content: flex-start; */ 
  text-align: left;
  z-index: 2;
  font-size: 3em;
  font-weight: 800;
}
</style>
