<template>
  <div class="footerBg bgColorLight">
    <div class>
      <b-container fluid="sm">
        <b-row>
          <b-col class="mb-3" md="6" lg="3">
            <div class="text-light aboutSoft">
              <h5 class="pb-3">ABOUT SoftLab NY</h5>
              <p>We are continuously digitizing the world around us. We deliver world class customer experiences.</p>
              <div>
                <nuxt-link to="/"><i class="fab fa-facebook-square h1 text-light pr-2"></i></nuxt-link>
                <nuxt-link to="/"><i class="fab fa-twitter-square h1 text-light pr-2"></i></nuxt-link>
                <nuxt-link to="/"><i class="fab fa-instagram-square h1 text-light pr-2"></i></nuxt-link>      
              </div>
            </div>
          </b-col>
          <b-col class="mb-3" md="6" lg="3">
            <div class="text-light">
              <h5 class="pb-3">SERVICES</h5>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">Web Development</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">Mobile Apps Development</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">Web & SAAS Applications</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">WordPress Development</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">E-Commerce Development</nuxt-link></div>
            </div>
          </b-col>
          <b-col class="mb-3" md="6" lg="3">
            <div class="text-light">
              <h5 class="pb-3">COMPANY</h5>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">About Us</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">Contact Us</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">Blog</nuxt-link></div>
              <div class="mb-1"><i class="fas fa-chevron-right text-light pr-1"></i><nuxt-link class="menuItem" to="/">Careers</nuxt-link></div>
            </div>
          </b-col>
          <b-col class="mb-3" md="6" lg="3">
            <div class="text-light ourMail">
              <h5 class="pb-3">JOIN OUR EMAIL LIST</h5>
              <p>Get 10% OFF your next project when you signup. Check your inbox for details.</p>
              <b-button block variant="primary" squared>GET STARTED</b-button>
            </div>
          </b-col>
        </b-row>
        <div class="pt-5" style="border-bottom: 1px solid white"></div>
        <div class="text-light text-center pt-3">
          <p>@2020 ReformedTech</p>
        </div>
      </b-container>
    </div>
  </div>
</template>

<script type="text/javascript">
export default {
  components: {},
};
</script>

<style scoped>
.footerBg {
  padding: 70px 0px 30px;
}
.aboutSoft p{
  font-size: 18px;
}
.ourMail p{
  font-size: 18px;
}
.menuItem {
  color: white;
  cursor: pointer;
  font-size: 18px;
}
.menuItem:hover {
  text-decoration: none;
  background-color: transparent;
  color: aqua;
}
</style>