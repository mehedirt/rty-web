<template>
  <div class="contactBody">
    <b-container fluid="sm">
      <div class="text-center hedlineContent pb-5">
        <h1>Get in Touch</h1>
        <p>Drop us a message and we will get back to you</p>
      </div>
      <b-row class="justify-content-center no-gutters">
        <b-col md="10" lg="5">
          <div class="addressContent">
            <h3 class="pb-3">Reach Us</h3>
            <div>
              <b-media class="pb-3">
                <template v-slot:aside>
                  <b-avatar size="2em" icon="star-fill">
                    <i class="fas fa-map-marker-alt"></i>
                  </b-avatar>
                </template>
                <h5 class>ReformedTech</h5>
                <h5>House: 32/1, Road: 3, Shyamoli, Dhaka.</h5>
              </b-media>
              <b-media class="pb-3">
                <template v-slot:aside>
                  <b-avatar size="2em" icon="star-fill">
                    <i class="fas fa-phone"></i>
                  </b-avatar>
                </template>
                <h5 class>+880 1303 094897</h5>
              </b-media>
              <b-media class="pb-3">
                <template v-slot:aside>
                  <b-avatar size="2em" icon="star-fill">
                    <i class="fas fa-paper-plane"></i>
                  </b-avatar>
                </template>
                <h5 class>contact@smartproperty.xyz</h5>
              </b-media>
              <b-media class>
                <template v-slot:aside>
                  <b-avatar size="2em" icon="star-fill">
                    <i class="fas fa-globe-asia"></i>
                  </b-avatar>
                </template>
                <h5 class>reformedtech.org</h5>
              </b-media>
            </div>
          </div>
        </b-col>
        <b-col md="10" lg="7">
          <div class="messageContent">
            <!-- <h3 class="pb-3">Say Something</h3> -->
            <div class="input-group flex-nowrap mt-4">
              <div class="w-100">
                <input
                  type="text"
                  class="form-control inputStyle mb-3"
                  placeholder="Your Name"
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
                <textarea
                  placeholder="Say Something..."
                  rows="3"
                  class="form-control inputStyle mb-3"
                ></textarea>
              </div>
            </div>
            <b-button
              class="py-3 font-weight-bold text-uppercase"
              block
              variant="primary"
              squared
            >send message</b-button>
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
  background: #ebf8fd;
  padding: 70px 0px;
}
.hedlineContent h1 {
  font-size: 48px;
}
.hedlineContent p {
  font-size: 25px;
}
.addressContent {
  background: white;
  padding: 24px 24px 24px 24px;
  height: 100%;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}
.messageContent {
  background: #6c757d;
  padding: 8px 24px 24px 24px;
  height: 100%;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}
.inputStyle {
  border-radius: 0;
  padding: 30px 10px;
}
</style>