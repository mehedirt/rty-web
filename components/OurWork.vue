<template>
  <div class="ourWork">
    <div class>
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h1>Our Works</h1>
          <p>Some examples of the web design and development projects we are grateful to have been a part of. Contact us to learn more about our projects.</p>
        </div>
        <b-row>
          <b-col v-for="(work,index) in workData" :key="index" class="pb-4" md="6" lg="4">
            <div class="pb-4">
              <b-img class :src="work.image" rounded fluid alt="Fluid image"></b-img>
            </div>
            <div class="text-center">
              <h4>{{work.title}}</h4>
              <p>{{work.description}}</p>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script type="text/javascript">
import workImage1 from "@/assets/images/Cabiy.png";
import workImage2 from "@/assets/images/Threefold.png";
import workImage3 from "@/assets/images/SeekFlat.png";
import workImage4 from "@/assets/images/SmartProperty.png";
import workImage5 from "@/assets/images/Lawlegal.png";
import workImage6 from "@/assets/images/berly.png";
export default {
  data: () => ({
    workData: [
      {
        image: workImage1,
        title: "Cabiy, NYC",
        description:
          "Cabiy is where you can connect with up to date listings for renting a car or finding a car to drive. Search through owners and drivers from multiple services like Yellow or Green cab, Uber, Lyft, Limos and much more in your location of choice.",
      },
      {
        image: workImage2,
        title: "THR3EFOLD",
        description:
          "THR3EFOLD believe fashion can positively impact people and planet but you can't build a business alone. So at THR3EFOLD, you gain access to a knowledgeable community where you can learn and find resources, search ethically certified factories around the world.",
      },
      {
        image: workImage3,
        title: "SeekFlat",
        description:
          "As per requirements and business needs, we are utilizing an agile methodology to complete this project, divided into the following phases.",
      },
      {
        image: workImage4,
        title: "SmartProperty",
        description:
          "SmartProperty is a collaborative, paperless, and social property management solution. It allows you to communicate with all of your residents or send messagesto particular persons or groups. Other than that, the solution has a social network embedded in it where residents can create profiles, share ideas, and plan for community activities together.",
      },
      {
        image: workImage5,
        title: "LawSuitLegal",
        description:
          "LawSuitLegal builds custom enterprise applications for the web and mobile devices. These solutions address process bottlenecks to improve efficiency, productivity and the bottom line for clients. alligatortek opens the possibilities for new strategies and business opportunities with software technologies.",
      },
      {
        image: workImage6,
        title: "BearlyMarketing",
        description:
          "BearlyMarketing builds custom enterprise applications for the web and mobile devices. These solutions address process bottlenecks to improve efficiency, productivity and the bottom line for clients. alligatortek opens the possibilities for new strategies and business opportunities with software technologies.",
      },
    ],
  }),
};
</script>

<style scoped>
.ourWork {
  padding: 70px 0px;
}
.hedlineContent h1 {
  font-size: 48px;
}
.hedlineContent p {
  font-size: 25px;
}
</style>