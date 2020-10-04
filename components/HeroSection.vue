<template>
  <div>
    <div class="heroWrap1" :style="`background-image: url(` + heroImage + `);`">
      <div class="heroContent">
        <b-container fluid>
          <b-row wrap>
            <b-col md="12" lg="7">
              <div class="heroHeading">
                <h1 class="text-light text-capitalize">
                  Simple Solution <br />
                  for your complex ideas...
                </h1>
                <p class="text-light">
                  SoftLabNewyork, a Group of Dynamic and Excellent Team of Web,
                  Mobile App, Software Developers, Strategic Consultants,
                  Marketing Advisors sits together and discusses your business
                  growth on a Technological Platform to maximize your
                  expectations above and beyond.
                </p>
              </div>
            </b-col>
            <b-col md="12" lg="5">
              <div
                class="d-flex justify-content-center justify-content-lg-end mb-3"
              >
                <b-card class="consutationStyle text-center">
                  <h2 class="text-light">GET A FREE</h2>
                  <h5 class="text-light">CONSULTATION</h5>
                  <div class="input-group flex-nowrap mt-4">
                    <div class="w-100">
                      <b-form-input
                        class="mb-3 inputStyle"
                        placeholder="Your Name"
                      ></b-form-input>
                      <b-form-input
                        class="mb-3 inputStyle"
                        placeholder="Email Address"
                      ></b-form-input>
                      <b-form-input
                        class="mb-3 inputStyle"
                        placeholder="Phone Number"
                      ></b-form-input>
                    </div>
                  </div>
                  <b-button class="text-uppercase getBtn" block squared
                    >Get Started</b-button
                  >
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
import heroImage from "@/assets/images/Abstract-Envelope.svg";
export default {
  data: () => ({
    heroImage: heroImage,
  }),
};
</script>

<style  scoped>
.heroWrap1 {
  background: center 50% no-repeat;
  background-size: cover;
}

.heroContent {
  padding: 180px 48px 50px 48px;
}
.heroHeading {
  padding: 50px 0px 0px 120px;
}
.heroHeading h1 {
  font-size: 60px;
  font-weight: 500;
  line-height: 1.3em;
}
.heroHeading p {
  font-size: 28px;
  line-height: 36px;
  font-weight: 500;
}
.getBtn {
  background: #056676;
  font-size: 1.2rem;
  padding: 0.9rem 1rem;
  border-color: #056676;
}

.inputStyle {
  border-radius: 0;
  background: rgba(163,210,202,0.1098);
  color: white;
  padding: 1.8rem 1rem;
  font-size: 1.2rem;
  border-color: #056676;
}
::placeholder {
  color: white;
  font-size: 1.2rem;
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
  .heroHeading {
    padding: 0px 0px 0px 0px;
  }
  .heroHeading h1 {
    font-size: 36px;
    line-height: 1.3em;
  }
  .heroHeading p {
    font-size: 18px;
    line-height: 32px;
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

@media screen and (max-width: 1100px) and (min-width: 992px) {
  .heroWrap {
    min-height: 650px;
  }
  .heroHeading {
    padding: 0 !important;
  }
  .heroHeading h1 {
    font-size: 38px;
    line-height: 1.3em;
  }
  .heroHeading p {
    font-size: 18px;
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
    line-height: 1.3em;
  }
  .heroHeading p {
    font-size: 20px;
    line-height: 36px;
  }
  .consutationStyle {
    width: 100%;
  }
}
</style>