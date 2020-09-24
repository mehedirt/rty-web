<template>
  <div class="ourPricing">
      <div class="">
          <b-container fluid="sm">
              <b-row class="text-light ">
                  <b-col class="align-self-center" md="12" lg="8">
                      <h1 class="text-lg-left text-center ">BEST PRICES IN THE INDUSTRY !</h1>
                  </b-col>
                  <b-col md="12" lg="4">
                      <div class="text-lg-right text-center ">
                         <p class="mb-0">STARTING AT ONLY</p> 
                         <h2 class="display-4 pr-2 font-weight-bold">$399</h2>
                         <p>(NO MONTHLY FEE)</p>
                      </div>
                  </b-col>
              </b-row>
              <b-row class="py-3 bgTextFeild align-items-center justify-content-around">
                  <b-col class="a">
                      <div> 
                          <input 
                      type="text"
                      class="form-control inputStyle mb-3 mb-lg-0 "
                      placeholder="Your Name"
                      aria-label="yourname"
                      aria-describedby="addon-wrapping"
                    />
                      </div>
                  </b-col>
                  <b-col class="a">
                      <input 
                      type="text"
                      class="form-control inputStyle mb-3 mb-lg-0"
                      placeholder="Company Name"
                      aria-label="Username"
                      aria-describedby="addon-wrapping"
                    />
                  </b-col>
                  <b-col class="a">
                      <input 
                      type="text"
                      class="form-control inputStyle mb-3 mb-lg-0"
                      placeholder="Your Email"
                      aria-label="Username"
                      aria-describedby="addon-wrapping"
                    />
                  </b-col>
                  <b-col class="a">
                      <input 
                      type="text"
                      class="form-control inputStyle mb-3 mb-lg-0"
                      placeholder="Your Phone"
                      aria-label="Username"
                      aria-describedby="addon-wrapping"
                    />
                  </b-col>
                  <b-col >
                      <b-button class="py-2" block variant="primary" squared>
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
    components: {
    },
  }
</script>

<style scoped>
    .ourPricing{
        background: black;
        padding: 70px 0px;
    }
    .bgTextFeild{
       background: #252525; 
    }
    .inputStyle{
  border-radius: 0;
  padding: 20px 10px;
}
  

::placeholder{
  color:black;
  font-weight: 500;
  text-transform: uppercase;
}
    .a{
        flex: 0 0 100%;
    }
    @media screen and (max-width: 991px) and (min-width: 576px) {
  .a {
    flex: 0 0 50%;
  }
}
  @media screen and (min-width: 992px) {
  .a {
    flex: 0 0 20%;
  }
}

</style>