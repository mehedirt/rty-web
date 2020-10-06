<template>
  <div>
      <AboutHeader :hero-image="heroImage"/>
      <AboutBody :about-image="aboutImage"/>
  </div>
</template>

<script>
import AboutHeader from '@/components/About/AboutHeader';
import AboutBody from '@/components/About/AboutBody';
import aboutImage from "@/assets/images/undraw_code_review_l1q9.svg";
import heroImage from "@/assets/images/header.svg";
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