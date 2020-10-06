<template>
  <div>
    <div class="aboutBody">
      <b-container fluid="sm">
        <div data-aos="fade-up" class="text-center hedlineContent pb-5">
          <h2>A journy with SoftLab</h2>
          <p>We shine when our clients do</p>
        </div>
        <b-row class="justify-content-center" >
          <b-col class="d-flex align-items-center" md="12" lg="6">
            <b-img data-aos="fade-right"
              class="mb-5"
              :src="aboutImage"
              rounded
              fluid
              alt="Fluid image"
            ></b-img>
          </b-col>
          <b-col md="12" lg="6">
            <div data-aos="fade-left" class="bodyContent">
              <h4>Who we are</h4>
              <hr />
              <p>
                Team SoftLab is a combination of software developers, technical
                experts and artistic designers who are working relentlessly and
                jointly to handle small and big projects. Our expert team
                members work hand in hand to reach our customer’s desirable
                result from every project and meet their promised vision. We are
                visionary, creative and obviously committed. We believe
                commitment is the core value of our work.
              </p>
              <h4>Industries we serve</h4>
              <hr />
              <p>
                SoftLab has been serving many clients around the world with
                amazing expertise in development, design & maintenance. With
                honesty we work and fulfill our commitment with all shapes of
                businesses. From start-ups to enterprises, all are our
                respective clients. Our strategic consultancy and creative web
                design/development give our customers a professional and result
                driven online presence which lifts our heart and makes us happy.
              </p>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div class="aboutBody1">
      <b-container fluid="sm">
        <b-row no-gutters>
          <b-col md="6" lg="3">
            <div data-aos="zoom-in" class="aboutClient aboutLight">
              <h4>7657</h4>
              <p>Our Satisfied & Happy <br> Customers</p>
            </div>
          </b-col>
          <b-col  md="6" lg="3">
            <div data-aos="zoom-in" class="aboutClient aboutDark">
              <h4>7</h4>
              <p>Years of Experience In <br> Business</p>
            </div>
          </b-col>
          <b-col class="order-md-2 order-lg-1"  md="6" lg="3">
            <div data-aos="zoom-in" class="aboutClient aboutLight ">
              <h4>1000</h4>
              <p>SoftLab Are Helping <br> Customers</p>
            </div>
          </b-col>
          <b-col class="order-md-1 order-lg-2" md="6" lg="3">
            <div data-aos="zoom-in" class="aboutClient aboutDark">
              <h4>2230</h4>
              <p>Hours Saved For Our <br> Clients</p>
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
    aboutImage: {
      type: String,
    },
  },
};
</script>

<style  scoped>
.aboutBody {
  padding: 70px 0px;
}
.aboutClient {
  height: 100%;
  color: white;
  text-align: center;
  padding: 40px 10px 15px;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}

.aboutLight{
  background:#399090 ;
}
.aboutDark{
  background:#056676 ;
  
}
.aboutBody1 {
  background: #ebf8fd;
  padding: 70px 0px;
}
.aboutClient h4{
  font-size: 40px;
  font-weight: 600;
}
.aboutClient p {
  font-size: 20px;
  font-weight: 500;
}
</style>