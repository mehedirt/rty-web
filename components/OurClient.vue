<template>
  <div class="ourClint bgColorDark">
    <b-container fluid="sm">
      <div class="text-center hedlineContent pb-5">
        <h2>Happy Clients</h2>
      </div>
      <carousel :responsive="{0:{items:1},768:{items:2}}" :autoplay="true" :dots="false" :margin="10" :nav="false">
        <div
          v-for="(client,index) in clientData"
          style=""
          :key="index"
          class="carouselContent"
        >
          <b-avatar class="caroselBody" size="3.5rem">
            <i class="fas fa-quote-left"></i>
          </b-avatar>
          <div class="carouselMessage">
            <p class="pt-3 clientMessage">{{client.message}}</p>
            <b-avatar :src="client.image" size="4.5rem"></b-avatar>
            <span class="clientTitle">{{client.name}}</span>
          </div>
        </div>
      </carousel>
    </b-container>
  </div>
</template>

<script type="text/javascript">
import heroImage from "@/assets/images/ban6.jpeg";
import clientImage1 from "@/assets/images/client1.jpeg";
import clientImage2 from "@/assets/images/client2.jpg";
import clientImage3 from "@/assets/images/client3.jpeg";
export default {
  data: () => ({
    clientData: [
      {
        name: "Elizabeth Harris",
        image: clientImage1,
        message:
          "ReformedTech has helped facilitate a great look and presence for our business.Our practice website has a design that is welcoming and informative with high optimization",
      },
      {
        name: "Adam Rodriguez",
        image: clientImage2,
        message:
          "ReformedTech Design did a great job for us. We may have been one of their picky	customers but they were always patient with our changes. We highly recommend Red Spot for website design. They are very responsive and quick when it comes to changes.",
      },
      {
        name: "Marissa Heredia",
        image: clientImage3,
        message:
          "We love working with ReformedTech! Not only do they create beautiful, interactive, easy-to-update websites, but they are also extremely helpful and amazing	to work with!",
      },
    ],
  }),
};
</script>

<style  scoped>
.ourClint {
  padding: 70px 0px;
}
.carouselContent{
  position: relative;
  padding-top:30px;
}
.caroselBody {
  position: absolute;
  left: 15px;
  top: 0px;
  z-index: 100;
  background: #F1F5F0;
  color:#14274e;
}
.carouselMessage{
  height: 100%;
  /* box-shadow: 0px 0px 5px 1px rgb(152 179 179 / 50%); */
  background: white;
  padding: 16px 8px 24px 16px;
  border-radius: 10px ;
}
.clientMessage{
  min-height: 130px;
  font-size: 18px;
}
.clientTitle{
  font-size: 26px;
  font-weight: 600;
  color: #14274e;
  margin-left: 10px;
}
</style>