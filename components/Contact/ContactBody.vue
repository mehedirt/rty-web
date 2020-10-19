<template>
  <div class="contactBody bgColorDark">
    <b-container fluid="sm">
      <div class="text-center hedlineContent pb-5">
        <h2>Get in Touch</h2>
        <p>Drop us a message and we will get back to you</p>
      </div>
      <b-row class="justify-content-center no-gutters">
        <b-col md="10" lg="5">
          <div class="bodyContent addressContent d-flex align-items-center">
            <!-- <h4 class="pb-3">Reach Us</h4> -->
            <div>
              <b-media class="pb-3">
                <template v-slot:aside>
                  <b-avatar size="2em" class="bgDark">
                    <i class="fas fa-map-marker-alt"></i>
                  </b-avatar>
                </template>
                <h5>House: 32/1, Road: 3, Shyamoli, Dhaka.</h5>
              </b-media>
              <b-media class="pb-3">
                <template v-slot:aside>
                  <b-avatar size="2em" class="bgDark">
                    <i class="fas fa-phone"></i>
                  </b-avatar>
                </template>
                <h5 class>+880 1303 094897</h5>
              </b-media>
              <b-media class="pb-3">
                <template v-slot:aside>
                  <b-avatar size="2em" class="bgDark">
                    <i class="fas fa-paper-plane"></i>
                  </b-avatar>
                </template>
                <h5 class>contact@smartproperty.xyz</h5>
              </b-media>
              <b-media class>
                <template v-slot:aside>
                  <b-avatar size="2em" class="bgDark">
                    <i class="fas fa-globe-asia"></i>
                  </b-avatar>
                </template>
                <h5 class>reformedtech.org</h5>
              </b-media>
            </div>
          </div>
        </b-col>
        <b-col md="10" lg="7">
          <div class="messageContent bgDark">
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
                <b-form-textarea
                  placeholder="Say Something..."
                  rows="3 "
                  class="inputStyle mb-3"
                ></b-form-textarea>
              </div>
            </div>
            <b-button class="getBtn" block squared>send message</b-button>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>  

<script type="text/javascript">
export default {
  data: () => ({}),
};
</script>

<style  scoped>
.contactBody {
  /* background: #ebf8fd; */
  padding: 100px 0px;
}

.addressContent {
  background: white;
  padding: 24px 24px 24px 24px;
  height: 100%;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}
.addressContent h4{
 color: #14274e;
}
.messageContent {
  padding: 8px 24px 24px 24px;
  height: 100%;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}
.getBtn {
  background: #ff5722;
  font-size: 1.2rem;
  padding: 0.9rem 1rem;
  border-color: #ff5722;
  text-transform: uppercase;
}

.inputStyle {
  border-radius: 0;
  background: #394867;
  color: white;
  padding: 1.8rem 1rem;
  font-size: 1.2rem;
  border-color: #394867;
}
::placeholder {
  color: #f1f6f9;
  font-size: 1.2rem;
  text-transform: uppercase;
}
</style>