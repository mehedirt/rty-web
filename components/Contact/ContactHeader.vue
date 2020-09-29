<template>
  <div>
    <div class="headerWrap" :style="`background-image: url(`+contactImage+`);`">
      <div class="headerContent">
        <b-container fluid>
          <div class="text-center text-light">
            <h1>Contact Us</h1>
            <div>
              <nuxt-link class="headerMenu" to="/">HOME</nuxt-link>
              <i class="fas fa-chevron-right text-light px-1"></i>
              <nuxt-link class="headerMenu" to="/contact">CONTACT</nuxt-link>
            </div>
          </div>
        </b-container>
      </div>
    </div>
  </div>
</template>  

<script type="text/javascript">
export default {
props: {
    contactImage:{ 
      type: String,
    }
  },
};
</script>

<style  scoped>




</style>