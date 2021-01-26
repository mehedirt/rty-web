<template>
  <div class="ourService">
    <b-container fluid="sm">
      <div v-if="false" class="hedlineContent pb-5">
        <h2>Our Services</h2>
        <p>
          Whether you’re in need of a website, mobile app or graphic design,
          Queens Web Design has all of your web and digital creative needs
          covered.
        </p>
      </div>
      <b-row class="justify-content-center">
        <b-col>
          <div class="hedlineContent hedlineAlignment">
            <h2 class="pb-3">Our Services</h2>
            <p>
              Whether you’re in need of a website, mobile app or graphic design,
              SoftLab has all of your web and digital creative needs covered.
            </p>
          </div>
        </b-col>
        <b-col
          v-for="(service, index) in serviceData"
          :key="index"
          class="mb-4"
          md="6"
          lg="4"
        >
          <div class="serviceContent">
            <b-img
              style="height: 50px"
              class="my-4"
              :src="service.icon"
              fluid
              alt="Responsive image"
            ></b-img>
            <h4>{{ service.title }}</h4>
            <p>{{ service.description }}</p>
            <b-button
              class="quateBtn"
              
              variant="outline"
              to="/getting-started"
              >Get a FREE Quate</b-button
            >
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script type="text/javascript">
import serviceImage from "@/assets/images/icon/web.svg";
import serviceImage2 from "@/assets/images/icon/mobile.svg";
import serviceImage3 from "@/assets/images/icon/saas.svg";
import serviceImage4 from "@/assets/images/icon/wordpress.svg";
import serviceImage5 from "@/assets/images/icon/e-commerce.svg";
export default {
  components: {},
  data: () => ({
    serviceData: [
      {
        icon: serviceImage,
        title: "WEB Development",
        description:
          "Use our creative community to get your perfect web site at a price that fits your budget",
      },
      {
        icon: serviceImage2,
        title: "Mobile Apps Development",
        description:
          "Regardless of the type of mobile app you have in mind, we have a solution that fits your business needs",
      },
      {
        icon: serviceImage3,
        title: "WEB & SAAS Applications",
        description:
          "We are offering you the best quality Software as a Service, because we develop software analyzing people's need",
      },
      {
        icon: serviceImage4,
        title: "WordPress Development",
        description:
          "Use our creative community to get your perfect & affordable WordPress development",
      },
      {
        icon: serviceImage5,
        title: "E-Commerce Development",
        description:
          "Our creative community is ready to build up your perfect e-commerce website for your business",
      },
    ],
  }),
};
</script>

<style scoped>
.ourService {
  padding: 100px 0px;
}
.hedlineAlignment{
  padding-top: 34px;
}
.serviceContent {
  background: white;
  padding: 16px 16px 24px 16px;
  /* text-align: center; */
  height: 100%;
  /* box-shadow: 0px 0px 10px 0px rgb(122 166 173 / 15%); */
  /* box-shadow: 0px 0px 10px 0px rgb(193 220 220 / 50%); */
  /* box-shadow: 0px 0px 10px 0px rgb(7 109 109 / 50%); */
  box-shadow: 1px 1px 4px 0px rgb(19 1 60 / 65%);
 
   transition: transform 200ms cubic-bezier(0.65, 0.94, 1, 1);
  border-radius: 10px;
}
.serviceContent:hover{
  transform: scale(1.04);
}
.serviceContent h4 {
  margin-bottom: 20px;
  color: #14274e;
  font-weight: 600;
}
.serviceContent p {
  margin-bottom: 20px;
  font-size: 18px;
}
.quateBtn {
  border-color: #14274e;
  color: black;
  font-weight: 500;
}
.quateBtn:hover {
  background: #14274e;
  color: white;
}
</style>