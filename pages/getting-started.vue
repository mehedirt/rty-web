<template>
  <div>
      <FreeQuateHeader :hero-image="heroImage"/>
      <FreeQuate/>
  </div>
</template>

<script>
import FreeQuate from '@/components/FreeQuate';
import FreeQuateHeader from '@/components/FreeQuateHeader';
import heroImage from "@/assets/images/hero1234.svg";
export default {
  components: {
     FreeQuate,
     FreeQuateHeader
    },
    asyncData(){
      return  {   
           heroImage: heroImage,
      }
    }
}
</script> 