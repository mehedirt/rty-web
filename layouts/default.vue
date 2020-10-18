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
      AOS.init(),
       function initFreshChat() {
    window.fcWidget.init({
      token: 'da7998db-7065-48a6-bccb-c2f1ed2e8954',
      host: 'https://wchat.freshchat.com'
    });
  }
  function initialize(i,t)
    {var e;i.getElementById(t)?initFreshChat():((e=i.createElement('script')).id=t,e.async=!0,e.src='https://wchat.freshchat.com/js/widget.js',e.onload=initFreshChat,i.head.appendChild(e))}function initiateCall(){initialize(document,'freshchat-js-sdk')}window.addEventListener?window.addEventListener('load',initiateCall,!1):window.attachEvent('load',initiateCall,!1);
    },
  }
</script>


