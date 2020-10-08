<template>
  <div>
    <div class="headerWrap" :style="`background-image: url(`+heroImage+`);`">
      <div class="headerContent">
        <b-container fluid>
          <div class="text-center text-light">
            <h1>Get a Quate</h1>
            <div>
              <p class="">It is a long established fact that a reader will be distracted by the readable <br> content of a page when looking at its layout</p>
              <b-button size="lg" class="btnBrand my-5">Start Now</b-button>
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
    heroImage:{ 
      type: String,
    }
  },

};
</script>

<style  scoped>

</style>