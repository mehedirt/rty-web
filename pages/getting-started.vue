<template>
  <div>
      <FreeQuateHeader :hero-image="heroImage"/>
      <FreeQuate/>
  </div>
</template>

<script>
import FreeQuate from '@/components/FreeQuate';
import FreeQuateHeader from '@/components/FreeQuateHeader';
import heroImage from "@/assets/images/header2.jpeg";
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