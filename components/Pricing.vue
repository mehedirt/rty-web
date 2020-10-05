<template>
  <div >
    <div class="ourPricing bglight">
      <b-container fluid="sm">
        <b-row class="text-light">
          <b-col class="align-self-center" md="12" lg="8">
            <h1 class="text-lg-left text-center">
              BEST PRICES IN THE INDUSTRY !
            </h1>
          </b-col>
          <b-col md="12" lg="4">
            <div class="text-lg-right text-center">
              <p class="mb-0">STARTING AT ONLY</p>
              <h2 class="display-4 font-weight-bold">$399</h2>
              <p>(NO MONTHLY FEE)</p>
            </div>
          </b-col>
        </b-row>
        <b-row
          class="py-3 bgTextFeild align-items-center justify-content-around"
        >
          <b-col class="msgPrice">
            <b-form-input
              class="inputStyle mb-3 mb-lg-0"
              v-model="text"
              placeholder="Your Name"
            ></b-form-input>
          </b-col>
          <b-col class="msgPrice">
            <b-form-input
              class="inputStyle mb-3 mb-lg-0"
              v-model="text"
              placeholder="Company Name"
            ></b-form-input>
          </b-col>
          <b-col class="msgPrice">
            <b-form-input
              class="inputStyle mb-3 mb-lg-0"
              v-model="text"
              placeholder="Your Email"
            ></b-form-input>
          </b-col>
          <b-col class="msgPrice">
            <b-form-input
              class="inputStyle mb-3 mb-lg-0"
              v-model="text"
              placeholder="Your Phone"
            ></b-form-input>
          </b-col>
          <b-col>
            <b-button class="py-2 getBtn" block  squared>
              GET STARTED
            </b-button>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script type="text/javascript">
export default {
  components: {},
  data() {
    return {
      text: ""
    }
  }
};
</script>

<style scoped>
.ourPricing {
 padding: 70px 0px;
}
.bgTextFeild {
 /* background: rgba(3,24,24,0.18039); */
 background: #a3d2ca;
}
.inputStyle {
  border-radius: 0;
  padding: 20px 10px;
  color: white;
  font-weight: 500;
  background: #399090;
  border: 1px solid #399090;
}

::placeholder {
  color: white;
  font-weight: 500;
  text-transform: uppercase;
}
.getBtn{
  background: #056676;
  font-size: 1rem;
  padding: 20px 10px;
  border-color: #056676;
  font-weight: 500;
  box-shadow: 0px 0px 10px 0px rgb(7 109 109 / 50%);
}
.msgPrice {
  flex: 0 0 100%;
}
@media screen and (max-width: 991px) and (min-width: 576px) {
  .msgPrice {
    flex: 0 0 50%;
  }
}
@media screen and (min-width: 992px) {
  .msgPrice {
    flex: 0 0 20%;
  }
}
</style>