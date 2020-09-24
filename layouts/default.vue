<template>
  <div>
    <HeaderComponent/>
    <Nuxt />
    <Footer/>
  </div>
</template>

<script type="text/javascript">
  import HeaderComponent from '@/components/HeaderComponent';
  
  import Footer from '@/components/Footer';

  export default {
    components: {
      HeaderComponent,
      Footer
    },
  }
</script>


