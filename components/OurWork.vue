<template>
  <div class="ourWork bgColorDark">
    <div class>
      <b-container fluid="sm">
        <div class="hedlineContent pb-5" data-aos="fade-up">
          <h2>Our Works</h2>
          <p>
            Some examples of the web design and development projects we are
            grateful to have been a part of. Contact us to learn more about our
            projects.
          </p>
        </div>
        <b-row no-gutters>
          <b-col
            v-for="(work, index) in workData"
            :key="index"
            md="12"
            lg="6"
            class="p-1"
          >
            <div class="workBody" data-aos="fade-up">
              <b-img
                class="pb-4"
                :src="work.image"
                fluid
                alt="Fluid image"
              ></b-img>

              <div class="workContent">
                <h4>{{ work.title }}</h4>
                <p>
                  <template v-if="seeMore === index">{{
                    work.description
                  }}</template>
                  <template v-else>{{
                    work.description.substr(0, 150) + ""
                  }}</template>
                  <span
                    class="seeMoreStyle"
                    v-if="seeMore === index"
                    @click="seeMore = null"
                    >See Less</span
                  >
                  <span class="seeMoreStyle" v-else @click="seeMore = index"
                    >...See More</span
                  >
                </p>
              </div>
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
    seeMore: null,
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
.workBody {
  padding: 20px;
  box-shadow: 0px 0px 10px 0px rgb(193 220 220 / 50%);
  height: 100%;
  background: white;
  border-radius: 10px;
}
.workContent {
  /* text-align: center; */
}

.workContent h4 {
  margin-bottom: 20px;
  font-weight: 600;
  color: #056676;
}
.workContent p {
  margin-bottom: 20px;
  font-size: 18px;
}
.seeMoreStyle {
  color: #056676;
  cursor: pointer;
  font-weight: 500;
}
</style>