<template>
  <div>
      <ContactHeader :hero-image="heroImage"/>
      <ContactBody/>
  </div>
</template>

<script>
import ContactHeader from '@/components/Contact/ContactHeader';
import ContactBody from '@/components/Contact/ContactBody';
import heroImage from "@/assets/images/contact111.jpg";
export default {
  components: {
      ContactHeader,
      ContactBody
    },
    asyncData(){
      return  {   
        heroImage: heroImage,
      }
    }
}
</script> 