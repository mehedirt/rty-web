<template>
  <div>
      <div class="aboutBody">
    <b-container fluid="sm">
      <div class="text-center hedlineContent pb-5">
        <h1>A journy with SoftLab</h1>
        <p>We shine when our clients do</p>
      </div>
      <b-row class="justify-content-center">
        <b-col class="d-flex  align-items-center" md="12" lg="6">
          <b-img class="" :src="aboutImage" rounded fluid alt="Fluid image"></b-img>
        </b-col>
        <b-col md="12" lg="6">
          <div>
            <h2>Who we are</h2>
            <p>Team SoftLab is a combination of software developers, technical experts and artistic designers who are working relentlessly and jointly to handle small and big projects. Our expert team members work hand in hand to reach our customer’s desirable result from every project and meet their promised vision. We are visionary, creative and obviously committed. We believe commitment is the core value of our work.</p>
            <h2>Industries we serve</h2> 
            <p>SoftLab has been serving many clients around the world with amazing expertise in development, design & maintenance. With honesty we work and fulfill our commitment with all shapes of businesses. From start-ups to enterprises, all are our respective clients. Our strategic consultancy and creative web design/development give our customers a professional and result driven online presence which lifts our heart and makes us happy.</p>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
  <div class="aboutBody1">
      <b-container fluid="sm">
          <b-row>
              <b-col md="6" lg="3">
                  <div class="text-center my-5 aboutClient">
                      <h1>7657</h1>
                  <p>Our Satisfied & Happy Customers</p>
                  </div>
              </b-col>
              <b-col md="6" lg="3">
                  <div class="text-center my-5 aboutClient">
                      <h1>7</h1>
                  <p>Years of Experience In Business</p>
                  </div>
              </b-col>
              <b-col md="6" lg="3">
                  <div class="text-center my-5 aboutClient">
                      <h1>1000</h1>
                  <p>SoftLab Are Helping Customers</p>
                  </div>
              </b-col>
              <b-col md="6" lg="3">
                  <div class="text-center my-5 aboutClient">
                      <h1>2230</h1>
                  <p>Hours Saved For Our Clients</p>
                  </div>
              </b-col>
          </b-row>
      </b-container>
  </div>
  </div>
</template>  

<script type="text/javascript">
export default {
  props: {
    aboutImage:{ 
      type: String,
    }
  },
  
};
</script>

<style  scoped>
.aboutBody {
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
.aboutBody1{
    background: #ebf8fd;
  padding: 70px 0px;
}
.aboutClient p{
    font-size: 20px;
}
</style>