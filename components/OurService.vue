<template>
  <div class="ourService bgColorDark">
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h2>Our Services</h2>
          <p>Whether you’re in need of a website, mobile app or graphic design, Queens Web Design has all of your web and digital creative needs covered.</p>
        </div>
        <b-row class="justify-content-center no-gutters">
          <b-col v-for="(service,index) in serviceData" :key="index" class="p-1 " md="6" lg="4">
              <div class="serviceContent">
                <b-img style="height: 120px;" class="my-4" :src="service.icon"   fluid alt="Responsive image"></b-img>
              <!-- <i :class="service.icon" class="display-2"></i> -->
              <h4>{{service.title}}</h4>
              <p>{{service.description}}</p>
              <b-button class="" squared variant="outline-secondary" to="/getting-started">Get a FREE Quate</b-button>
              </div>
              
          </b-col>
        </b-row>
      </b-container>
  </div>
</template>

<script type="text/javascript">
import serviceImage from "@/assets/images/icon/website.png";
import serviceImage2 from "@/assets/images/icon/mobile2.png";
import serviceImage3 from "@/assets/images/icon/sass.png";
import serviceImage4 from "@/assets/images/icon/wordpress.png";
import serviceImage5 from "@/assets/images/icon/ecom1.png";
export default {
  components:{
    
  },
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
  padding: 70px 0px;
}
.serviceContent {
  background: white;
  padding: 16px 8px 24px 8px;
  text-align: center;
  height: 100%;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}
.serviceContent h4{
  margin-bottom: 20px;
}
.serviceContent p{
  margin-bottom: 20px;
  font-size: 18px;
}
</style>