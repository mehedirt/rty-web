<template>
  <div class="ourService">
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h1>Our Services</h1>
          <p>Whether you’re in need of a website, mobile app or graphic design, Queens Web Design has all of your web and digital creative needs covered.</p>
        </div>
        <b-row class="justify-content-center">
          <b-col v-for="(service,index) in serviceData" :key="index" class="pb-4" md="6" lg="4">
            <div class="serviceContent">
              <i :class="service.icon" class="display-2"></i>
              <h4>{{service.title}}</h4>
              <p>{{service.description}}</p>
              <b-button squared variant="outline-secondary">Get a FREE Quate</b-button>
            </div>
          </b-col>
        </b-row>
      </b-container>
  </div>
</template>

<script type="text/javascript">
export default {
  data: () => ({
    serviceData: [
      {
        icon: "fab fa-accusoft",
        title: "WEB Development",
        description:
          "Use our creative community to get your perfect web site at a price that fits your budget",
      },
      {
        icon: "fab fa-accusoft",
        title: "Mobile Apps Development",
        description:
          "Regardless of the type of mobile app you have in mind, we have a solution that fits your business needs",
      },
      {
        icon: "fab fa-accusoft",
        title: "WEB & SAAS Applications",
        description:
          "We are offering you the best quality Software as a Service, because we develop software analyzing people's need",
      },
      {
        icon: "fab fa-wordpress",
        title: "WordPress Development",
        description:
          "Use our creative community to get your perfect & affordable WordPress development",
      },
      {
        icon: "fab fa-amazon-pay",
        title: "E-Commerce Development",
        description:
          "Our creative community is ready to build up your perfect e-commerce website",
      },
    ],
  }),
};
</script>

<style scoped>
.ourService {
  background: #ebf8fd;
  padding: 70px 0px;
}
.hedlineContent h1 {
  font-size: 48px;
}
.hedlineContent p {
  font-size: 25px;
}
.serviceContent {
  background: white;
  padding: 16px 8px 24px 8px;
  text-align: center;
  height: 100%;
  box-shadow: 0px 24px 48px -13px rgba(0, 0, 0, 0.05);
}
</style>