<template>
  <div>
      <AboutHeader :hero-image="heroImage"/>
      <AboutBody :about-image="aboutImage"/>
  </div>
</template>

<script>
import AboutHeader from '@/components/About/AboutHeader';
import AboutBody from '@/components/About/AboutBody';
import aboutImage from "@/assets/images/about-us.jpeg";
import heroImage from "@/assets/images/header2.jpeg";
export default {
  components: {
      AboutHeader, 
      AboutBody
    },
    asyncData(){
      return  {
        aboutImage : aboutImage, 
        heroImage: heroImage,
      }
    }
    
}
</script>