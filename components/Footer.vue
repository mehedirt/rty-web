<template>
  <div class="footerBg bglight">
    <div class>
      <b-container fluid="sm">
        <b-row class="footerHeading">
          <b-col class="mb-3" md="6" lg="4">
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
          <b-col class="mb-3" md="6" lg="2">
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
              <h5 class="pb-3">JOIN WITH US</h5>
              <p>Get 10% OFF your next project when you signup. Check your inbox for details.</p>
              <b-button class="getBtn" block squared>GET STARTED</b-button>
            </div>
          </b-col>
        </b-row>
        <hr>
        <div class="text-light text-center pt-3">
          <div class="copyRight">
            <p>&copy; 2020 <nuxt-link class="copyLink"  to="/">ReformedTech</nuxt-link>, All rights reserved.</p>
          </div>
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
.getBtn {
  background: #056676;
  padding: 0.5rem 1rem;
  border-color: #056676;
}
.copyRight{
  font-size: 18px;
}
.copyLink{
  color:#e8ded2;
  cursor: pointer;
  font-size: 18px
}

.copyLink:hover { 
  text-decoration: none;
  background-color: transparent;
  color: aqua;
}
.footerHeading h5{
  font-size: 23px;
  font-weight: 600;
}
</style>