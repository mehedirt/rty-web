<template>
  <div class="ourClint">
    <b-container fluid="sm">
      <div class="text-center hedlineContent pb-5">
        <h1>Happy Clients</h1>
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
          <b-card style="height:100%;">
            <p class="pt-3 clientMessage">{{client.message}}</p>
            <b-avatar :src="client.image" size="4.5rem"></b-avatar>
            <span class="h4 pl-2">{{client.name}}</span>
          </b-card>
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
  background: #ebf8fd;
  padding: 70px 0px;
}
.hedlineContent h1 {
  font-size: 48px;
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
  background: #ebf8fd;
  color:black;
}
.clientMessage{
  min-height: 130px;
}
</style>