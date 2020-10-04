<template>
  <div>
    <HeroSection/>
    <OurService/>
    <OurWork/>
    <Pricing/>
    <OurClient/>
  </div>
</template>

<script>
import HeroSection from '@/components/HeroSection';
import OurService from '@/components/OurService';
import OurWork from '@/components/OurWork';
import OurClient from '@/components/OurClient';
import Pricing from '@/components/Pricing';
export default {
  components: {
      HeroSection,
      OurService,
      OurWork,
      OurClient,
      Pricing,
    },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
