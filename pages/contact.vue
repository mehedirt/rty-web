<template>
  <div>
      <ContactHeader :contact-image="headerImage"/>
      <ContactBody/>
  </div>
</template>

<script>
import ContactHeader from '@/components/Contact/ContactHeader';
import ContactBody from '@/components/Contact/ContactBody';
import topImage from "@/assets/images/header2.jpeg";
export default {
  components: {
      ContactHeader,
      ContactBody
    },
    asyncData(){
      return  {   
        headerImage: topImage,
      }
    }
}
</script> 