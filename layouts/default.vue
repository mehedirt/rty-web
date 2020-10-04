<template>
  <div>
    <Header/>
    <Nuxt />
    <Footer/>
  </div>
</template>

<script type="text/javascript">
  import Header from '@/components/Header';
  import Footer from '@/components/Footer';
  import AOS from 'aos';
import 'aos/dist/aos.css';

  export default {
    components: {
      Header,
      Footer
    },
    mounted () {
      AOS.init()
    },
  }
</script>


