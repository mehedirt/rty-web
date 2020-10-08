<template>
  <div>
      <PricingHeader :hero-image="heroImage"/>
      <PricingBody />
  </div>
</template>

<script>
import PricingHeader from '@/components/Pricing/PricingHeader';
import PricingBody from '@/components/Pricing/PricingBody';
// import aboutImage from "@/assets/images/undraw_code_review_l1q9.svg";
import heroImage from "@/assets/images/header.svg";
export default {
  components: {
    PricingHeader,
    PricingBody
    },
    asyncData(){
      return  {
        // aboutImage : aboutImage, 
        heroImage: heroImage,
      }
    }
    
}
</script>