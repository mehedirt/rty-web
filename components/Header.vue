<template>
  <div>
    <div class="heroWrap" :style="`background-image: url(`+heroImage+`);`">
      <div class="heroContent">
        <b-container fluid>
          <b-row>
            <b-col md="12" lg="7" >
              <div class="heroHeading d-none d-lg-block ">
                <h1 class="text-light">
                  SIMPLE SOLUTION FOR YOUR COMPLEX IDEAS...
                </h1>
                <p
                  class="text-light"
                >SoftLabNewyork, a Group of Dynamic and Excellent Team of Web, Mobile App, Software Developers, Strategic Consultants, Marketing Advisors sits together and discusses your business growth on a Technological Platform to maximize your expectations above and beyond.</p>
              </div>
            </b-col>
            <b-col  md="12" lg="5">
              <div class="d-flex justify-content-center justify-content-lg-end">
                <b-card class="consutationStyle text-center w-75">
                  <h2 class="font-weight-bold text-light">GET A FREE</h2>
                  <h3 class="text-light">CONSULTATION</h3>
                  <div class="input-group flex-nowrap mt-4">
                    <div class="w-100">
                      <input
                        type="text"
                        class="form-control inputStyle mb-3"
                        placeholder="User name"
                        aria-label="Username"
                        aria-describedby="addon-wrapping"
                      />
                      <input
                        type="text"
                        class="form-control inputStyle mb-3"
                        placeholder="Email Address"
                        aria-label="Emailaddress"
                        aria-describedby="addon-wrapping"
                      />
                      <input
                        type="text"
                        class="form-control inputStyle mb-3"
                        placeholder="Phone Number"
                        aria-label="Phonenumber"
                        aria-describedby="addon-wrapping"
                      />
                    </div>
                  </div>
                  <b-button class="py-3 font-weight-bold text-uppercase" block variant="primary" squared>Get Started</b-button>
                </b-card>
              </div>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </div>
    <div class="heroNav">
      <b-navbar toggleable="lg" class="navBarStyle" :class="[isNavFixed ? 'fixed': '']">
        <b-navbar-brand href="#" >
          <div class="text-light h2 text-uppercase">SoftLab.ny Web</div>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="mx-auto">          
            <b-nav-item ><nuxt-link class="menuItem" to="/">HOME</nuxt-link></b-nav-item>
            <b-nav-item ><nuxt-link class="menuItem" to="/">ABOUT</nuxt-link></b-nav-item>
            <b-nav-item ><nuxt-link class="menuItem" to="/">MAKETING</nuxt-link></b-nav-item>
            <b-nav-item ><nuxt-link class="menuItem" to="/">PORTFOLIO</nuxt-link></b-nav-item>
            <b-nav-item ><nuxt-link class="menuItem" to="/">BLOG</nuxt-link></b-nav-item>
            <b-nav-item ><nuxt-link class="menuItem" to="/">CONTACT</nuxt-link></b-nav-item>
          </b-navbar-nav>
          <b-navbar-brand href="#">
            <b-button class="px-3 py-3" squared>
              <span class="h4">017-17-295656</span>
            </b-button>
          </b-navbar-brand>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>  

<script type="text/javascript">
import heroImage from "@/assets/images/ban6.jpeg";
  export default {
    data: () => ({
        heroImage: heroImage,
        isNavFixed: false,
        showNavbarLogo: true,
        showNavbarTitle: false,
        showGetStartedButton: false,
        showMobileMenu: false,
    }),
    mounted() {
        const toggleFixedNavbar = () => {
            if(document.body.scrollTop > 80 || document.documentElement.scrollTop > 80){
                this.isNavFixed = true
            }else{
                this.isNavFixed = false;
            }
        }

        const handleOnScroll = ()=> {
            toggleFixedNavbar();
            if(document.body.scrollTop > 80 || document.documentElement.scrollTop > 80){
                this.showNavbarLogo = false;
                this.showNavbarTitle = true;
                this.showGetStartedButton = true;
            }else{
                this.showNavbarLogo = true;
                this.showNavbarTitle = false;
                this.showGetStartedButton = false;
            }
        }

        const scrollEvent = window.addEventListener('scroll', handleOnScroll)
        this.$once('hook:beforeDestroy', ()=>{
            window.removeEventListener(scrollEvent, handleOnScroll)
        })
    },
    methods: {
        toggleMenu() {
            this.showMobileMenu = !this.showMobileMenu;
        },
         menuTrack(e){
            const link_text = e.target.innerText
            dataLayer.push({
                event: 'Click-Menu',
                label: this.$route.path,
                action: 'select - ' + link_text,
                noninteraction: false
            })
        }
       
    }
}
</script>
<style  scoped>
.heroWrap {
  width: 100%;
  min-height: 800px;
  position: inherit;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top center;
  position: relative;
  z-index: 0;

}
.heroNav {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
}
.heroContent {
  width: 100%;
  position: absolute;
  top: 190px;
  left: 0;
  padding: 0px 48px;
}
.heroHeading{
  padding: 50px 0px 0px 120px;
}
.heroHeading h1{
  font-size: 60px;
  font-weight: 300;
  line-height: 1.3em;
}
.heroHeading p{
  font-size: 28px;
  line-height: 36px;
}
.navBarStyle{
  padding: 0px 50px;
  height: 120px;
}
.fixed{
  position: absolute;
  left: 0px;
  top: 0px;
  width: 100%;
  background: #252525;
  box-shadow: 0 2px 2px 0 rgba(0,0,0,0.15);
  z-index: 11111111111;
}
.menuItem{
  color: white;
  font-size: 18px;
  font-weight: 500;
  padding: 0px 5px;
  cursor: pointer;
}
.menuItem:hover{
  text-decoration: none;
  background-color: transparent;
  color: aqua;
}

.inputStyle{
  border-radius: 0;
  padding: 30px 10px;
}
::placeholder{
  color:black;
  font-weight: 500;
  text-transform: uppercase;
}
.consutationStyle{
  background: rgba(000,000,000, 0.4); 
}

</style>