<template>
  <div>
    <div class="heroNav">
      <b-navbar
        toggleable="lg"
        class="navBarStyle"
        :class="[isNavFixed ? 'fixed' : '']"
      >
        <!-- <span></span> -->
        <b-navbar-brand class="mr-0" href="#">
          <div class="text-light text-center">
            <h2>SoftLab.NY</h2>
          </div>
          <div class="contactNumber d-block d-lg-none">
            <span>017-1729-5256</span>
          </div>
        </b-navbar-brand>
        <span class="d-lg-none toggleIconStyle" @click="showToggleNavbar">
          <i class="fas fa-bars toggleIcon pr-3"></i>
        </span>
        <transition name="slide">
          <b-collapse
            class="collapseBg"
            v-if="toggle"
            is-nav
            :style="toggle ? 'display: block' : 'display: none'"
          >
            <b-navbar-nav class="mx-auto">
              <b-nav-item class="menuItemStyle">
                <nuxt-link class="menuItem" to="/">HOME</nuxt-link>
              </b-nav-item>
              <b-nav-item class="menuItemStyle">
                <nuxt-link class="menuItem" to="/about">ABOUT</nuxt-link>
              </b-nav-item>
              <b-nav-item class="menuItemStyle">
                <nuxt-link class="menuItem" to="/">PORTFOLIO</nuxt-link>
              </b-nav-item>
              <b-nav-item class="menuItemStyle">
                <nuxt-link class="menuItem" to="/">BLOG</nuxt-link>
              </b-nav-item>
              <b-nav-item class="menuItemStyle menuItemStyle2">
                <nuxt-link class="menuItem" to="/contact">CONTACT</nuxt-link>
              </b-nav-item>
            </b-navbar-nav>
            <b-navbar-brand href="#" class="d-none d-lg-block">
              <div class="contactNumber">
                <span>017-1729-5256</span>
              </div>
            </b-navbar-brand>
          </b-collapse>
        </transition>
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
    toggle: false,
    mobileNav: false,
    toggleStage: false,
  }),
  mounted() {
    const toggleFixedNavbar = () => {
      if (
        document.body.scrollTop > 80 ||
        document.documentElement.scrollTop > 80
      ) {
        this.isNavFixed = true;
      } else {
        this.isNavFixed = false;
      }
    };

    const handleOnScroll = () => {
      toggleFixedNavbar();
      if (
        document.body.scrollTop > 80 ||
        document.documentElement.scrollTop > 80
      ) {
        this.showNavbarLogo = false;
        this.showNavbarTitle = true;
        this.showGetStartedButton = true;
      } else {
        this.showNavbarLogo = true;
        this.showNavbarTitle = false;
        this.showGetStartedButton = false;
      }
    };

    const scrollEvent = window.addEventListener("scroll", handleOnScroll);
    this.$once("hook:beforeDestroy", () => {
      window.removeEventListener(scrollEvent, handleOnScroll);
    });
    //for mobile navbar screen resize
    const handleResize = () => {
      if (window.innerWidth < 992) {
        this.toggle = false;
        this.toggleStage = true;
        if (this.toggleStage && this.mobileNav) {
          this.toggle = true;
        }
      } else {
        this.toggle = true;
      }
    };
    window.addEventListener("resize", handleResize);
    this.$once("hook:beforeDestroy", () => {
      window.removeEventListener("resize", handleResize);
    });
    handleResize();
  },
  methods: {
    toggleMenu() {
      this.showMobileMenu = !this.showMobileMenu;
    },
    menuTrack(e) {
      const link_text = e.target.innerText;
      dataLayer.push({
        event: "Click-Menu",
        label: this.$route.path,
        action: "select - " + link_text,
        noninteraction: false,
      });
    },
    showToggleNavbar() {
      this.toggle = !this.toggle;
      this.mobileNav = !this.mobileNav;
    },
  },
};
</script>

<style  scoped>
.heroNav {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 111111111111111111;
}
.navBarStyle {
  padding: 0px 0px;
  position: relative;
  justify-content: center;
}
.fixed {
  position: absolute;
  left: 0px;
  top: 0px;
  width: 100%;
  background: #399090;
  box-shadow: 0 2px 2px 0 rgb(29 111 110 / 53%);
  z-index: 11111111111;
}
.menuItemStyle {
  border-top: 1px solid #5eaaa8;
}
.menuItemStyle:hover {
  background: #056676;
}
.menuItemStyle2 {
  border-bottom: 1px solid #5eaaa8;
}
.menuItem {
  color: white;
  font-size: 18px;
  font-weight: 500;
  padding: 0px 5px;
  cursor: pointer;
}
.menuItem:hover {
  text-decoration: none;
  background-color: transparent;
  color: aqua;
}
.contactNumber {
  background: #056676;
  color: white;
  padding: 6px 8px;
  font-size: 24px;
  font-weight: 700;
  box-shadow: 0px 0px 10px 0px rgb(7 109 109 / 50%);
}
.toggleIconStyle {
  position: absolute;
  top: 38px;
  right: 0;
}
.toggleIcon {
  color: white;
  font-size: 30px;
  cursor: pointer;
}
.collapseBg {
  background: #399090;
  text-align: center;
}
.navbar-light .navbar-toggler {
  color: none !important;
  border-color: none !important;
}
.navbar-toggler {
  padding: 0.25rem 0.75rem;
  font-size: 1.25rem;
  line-height: 1;
  background-color: transparent;
  border: none !important;
  border-radius: none !important;
}

@media screen and (min-width: 992px) {
  .navBarStyle {
    padding: 20px 50px;
  }
  .collapseBg {
    background: transparent;
  }
  .menuItemStyle {
    border-top: 0px;
  }
  .menuItemStyle:hover {
    background: none;
  }
  .menuItemStyle2 {
    border-bottom: 0px;
  }
}

.slide-enter-active {
  -moz-transition-duration: 0.3s;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -moz-transition-timing-function: ease-in;
  -webkit-transition-timing-function: ease-in;
  -o-transition-timing-function: ease-in;
  transition-timing-function: ease-in;
}
.slide-leave-active {
  -moz-transition-duration: 0.3s;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -moz-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  -webkit-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  -o-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
}
.slide-enter-to,
.slide-leave {
  max-height: 100px;
  overflow: hidden;
}
.slide-enter,
.slide-leave-to {
  overflow: hidden;
  max-height: 0;
}
</style>