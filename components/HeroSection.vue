<template>
  <div>
    <div class="heroWrap" :style="`background-image: url(`+heroImage+`);`">
      <div class="heroContent">
        <b-container fluid>
          <b-row wrap>
            <b-col md="12" lg="7">
              <div class="heroHeading d-none d-md-block">
                <h1 class="text-light text-capitalize">Simple Solution for your complex ideas...</h1>
                <p
                  class="text-light"
                >SoftLabNewyork, a Group of Dynamic and Excellent Team of Web, Mobile App, Software Developers, Strategic Consultants, Marketing Advisors sits together and discusses your business growth on a Technological Platform to maximize your expectations above and beyond.</p>
              </div>
            </b-col>
            <b-col md="12" lg="5">
              <div class="d-flex justify-content-center justify-content-lg-end">
                <b-card class="consutationStyle text-center">
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
                  <b-button
                    class="py-3 font-weight-bold text-uppercase"
                    block
                    variant="primary"
                    squared
                  >Get Started</b-button>
                </b-card>
              </div>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </div>
  </div>
</template>  

<script type="text/javascript">
import heroImage from "@/assets/images/ban6.jpeg";
export default {
  data: () => ({
    heroImage: heroImage,
  }),
};
</script>

<style  scoped>
.heroWrap {
  width: 100%;
  min-height: 750px;
  position: inherit;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top center;
}

.heroContent {
  padding: 180px 48px 0px 48px;
}
.heroHeading {
  padding: 50px 0px 0px 120px;
}
.heroHeading h1 {
  font-size: 60px;
  font-weight: 300;
  line-height: 1.3em;
}
.heroHeading p {
  font-size: 28px;
  line-height: 36px;
}

.inputStyle {
  border-radius: 0;
  padding: 30px 10px;
}
::placeholder {
  color: black;
  font-weight: 500;
  text-transform: uppercase;
}
.consutationStyle {
  background: rgba(000, 000, 000, 0.4);
  width: 80%;
}

@media screen and (max-width: 768px) {
  .heroWrap {
  min-height: 650px;
}
  .heroContent {
  padding: 180px 0px 0px 0px;
}
.consutationStyle {
  width: 100%;
}
}
@media screen and (max-width: 992px) and (min-width: 768px) {
  .heroWrap {
  min-height: 880px;
}
  .heroHeading {
  padding: 0;
}
.heroHeading h1 {
  font-size: 40px;
  font-weight: 300;
  line-height: 1.3em;
}
.heroHeading p {
  font-size: 20px;
  line-height: 28px;
}

}


@media screen and (max-width: 1100px) and (min-width: 992px) {
  .heroWrap {
    min-height: 650px;
  }
  .heroHeading {
    padding: 0 !important;
  }
  .heroHeading h1 {
    font-size: 40px;
    font-weight: 300;
    line-height: 1.3em;
  }
  .heroHeading p {
    font-size: 20px;
    line-height: 28px;
  }
  .consutationStyle {
    width: 100%;
  }
}
@media screen and (max-width: 1600px) and (min-width: 1100px) {
  .heroWrap {
    min-height: 700px;
  }
  .heroHeading {
    padding: 20px 0px 0px 30px;
  }
  .heroHeading h1 {
    font-size: 45px;
    font-weight: 300;
    line-height: 1.3em;
  }
  .heroHeading p {
    font-size: 20px;
    line-height: 28px;
  }
  .consutationStyle {
    width: 100%;
  }
}
</style>