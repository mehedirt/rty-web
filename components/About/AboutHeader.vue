<template>
  <div>
    <div class="heroWrap" :style="`background-image: url(`+heroImage+`);`">
      <div class="heroContent">
        <b-container fluid>
          <div class="text-center text-light">
            <h1>About Us</h1>
            <div>
              <nuxt-link class="heroMenu" to="/">HOME</nuxt-link>
              <i class="fas fa-chevron-right text-light px-1"></i>
              <nuxt-link class="heroMenu" to="/about">ABOUT</nuxt-link>
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
.heroWrap {
  width: 100%;
  min-height: 500px;
  position: inherit;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top center;
}

.heroContent {
  padding: 220px 48px 0px 48px;
}

.heroMenu {
  color: white;
  font-size: 18px;
  font-weight: 500;
  padding: 0px 5px;
  cursor: pointer;
}
.heroMenu:hover {
  text-decoration: none;
  background-color: transparent;
  color: aqua;
}
</style>