<template>
  <div>
    <div class="pricingBody">
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h2>Pricing</h2>
          <p>Let introduce to our plan</p>
        </div>
        <div>
          <b-table
            responsive="sm"
            hover
            :bordered="bordered"
            :outlined="outlined"
            :fields="fields"
            :items="pricingData"
            thead-tr-class="rowClass"
            tbody-tr-class="colomnClass"
            caption-top
          >
            <template v-slot:table-caption>
              <h2 class="textBrand ">
                The Cost of Digital Marketing 2020
              </h2>
            </template>
            <template v-slot:head(View_services)="data">
              <div class="text-center">View Services</div>
            </template>

            <template v-slot:cell(View_services)="data">
              <div class="text-center">
                <b-button class="btnBrand" size="sm">View Details</b-button>
              </div>
            </template>
          </b-table>
        </div>
      </b-container>
    </div>
    <div class="pricingExample bgColorDark">
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h2>Recent Examples</h2>
          <p>
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.
          </p>
        </div>
        <div>
          <b-row no-gutters>
            <b-col
              class="p-3"
              lg="6"
              v-for="(example, index) in exampleData"
              :key="index"
            >
              <div class="exampleContent">
                  <div class="text-center d-block d-lg-none pb-3">
                      <span class="priceStyle">{{ example.price }}</span>
                      <!-- <br /> -->
                      <span class="durationStyle pl-2">{{ example.duration }}</span>
                    </div>
                <b-media no-body>
                    
                  <b-media-aside   vertical-align="center">
                    <div class="text-center d-none d-lg-block">
                      <span class="priceStyle">{{ example.price }}</span>
                      <br />
                      <span class="durationStyle">{{ example.duration }}</span>
                    </div>
                  </b-media-aside>

                  <b-media-body class="pl-2">
                    <h4>{{ example.title }}</h4>
                    <p>{{ example.description }}</p>
                  </b-media-body>
                </b-media>
              </div>
            </b-col>
          </b-row>
        </div>
      </b-container>
    </div>
    <div class="askQuestion">
      <b-container fluid="sm">
        <div class="text-center hedlineContent pb-5">
          <h2 class="subheading">FAQ</h2>
          <p>Frequently Asked Questions</p>
        </div>
        <div class="">
          <b-row class="d-flex justify-content-center">
            <b-col lg="9" class="mb-3">
              <div class="questionItem">
                <b-media right-align>
                  <template v-slot:aside>
                    <span @click="showFAQ = !showFAQ" class="h5 iconStyle"
                      ><i
                        :class="
                          !showFAQ ? 'fas fa-chevron-down' : 'fas fa-chevron-up'
                        "
                      ></i
                    ></span>
                  </template>
                  <span class="h5">Q1. What is Lorem Ipsum?</span>
                </b-media>
                <div class="py-2 px-3" v-if="showFAQ">
                  <span class="answerItem"
                    >Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.</span
                  >
                </div>
              </div>
            </b-col>
            <b-col lg="9" class="mb-3">
              <div class="questionItem">
                <b-media right-align>
                  <template v-slot:aside>
                    <span @click="showFAQ2 = !showFAQ2" class="h5 iconStyle"
                      ><i
                        :class="
                          !showFAQ2
                            ? 'fas fa-chevron-down'
                            : 'fas fa-chevron-up'
                        "
                      ></i
                    ></span>
                  </template>
                  <span class="h5">Q2. Why do we use it?</span>
                </b-media>
                <div class="py-2 px-3" v-if="showFAQ2">
                  <span class="answerItem">
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </span>
                </div>
              </div>
            </b-col>
            <b-col lg="9">
              <div class="questionItem">
                <b-media right-align>
                  <template v-slot:aside>
                    <span @click="showFAQ3 = !showFAQ3" class="h5 iconStyle"
                      ><i
                        :class="
                          !showFAQ3
                            ? 'fas fa-chevron-down'
                            : 'fas fa-chevron-up'
                        "
                      ></i
                    ></span>
                  </template>
                  <span class="h5"> Q3. Where does it come from? </span>
                </b-media>
                <div class="py-2 px-3" v-if="showFAQ3">
                  <span class="answerItem">
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </span>
                </div>
              </div>
            </b-col>
          </b-row>
        </div>
      </b-container>
    </div>
  </div>
</template>  

<script type="text/javascript">
export default {
  data: () => ({
    showFAQ: true,
    showFAQ2: false,
    showFAQ3: false,
    outlined: false,
    bordered: true,
    fields: ["Service_Name", "Generel_Service_cost", "View_services"],
    pricingData: [
      {
        Service_Name: "Search Engine Optimization (SEO)",
        Generel_Service_cost: "$500-$30000+ Per month",
      },
      {
        Service_Name: "Pay-per-click Advertising (PPC)",
        Generel_Service_cost: "2-20% of monthly ad spend",
      },
      {
        Service_Name: "Email Marketing",
        Generel_Service_cost: "$000-$5,000/month or $0.1-$0.5/email",
      },
      {
        Service_Name: "Social Media Marketing",
        Generel_Service_cost: "$250-$10,000/month",
      },
      {
        Service_Name: "Web Design",
        Generel_Service_cost: "$2,500-$100k",
      },
    ],
    exampleData: [
      {
        price: "$40K",
        duration: "3 Months",
        title: "Community Management Platform",
        description:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        price: "$18K",
        duration: "2 Months",
        title: "Arts Marketplace",
        description:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        price: "$40K",
        duration: "5 Months",
        title: "API Middleware Connector",
        description:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        price: "$40K",
        duration: "6 Months",
        title: "Proptech Cloud",
        description:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
    ],
  }),
};
</script>

<style scope>
.pricingBody {
  /* background: #ebf8fd; */
  padding: 70px 0px;
}
.rowClass {
  background: #056676;
  color: white;
  font-size: 22px;
}
.colomnClass {
  /* background: #399090;
  color: white; */
  font-size: 20px;
}

.pricingExample {
  padding: 70px 0px;
}
.exampleContent {
  background: white;
  padding: 24px 16px 24px 16px;
  /* text-align: center; */
  height: 100%;
  box-shadow: 0px 0px 10px 0px rgb(7 109 109 / 50%);
}
.exampleContent h4 {
  margin-bottom: 20px;
  color: #056676;
  font-weight: 600;
}
.exampleContent p {
  margin-bottom: 20px;
  font-size: 18px;
}
.priceStyle {
  font-size: 60px;
  font-weight: 600;
}
.durationStyle {
  font-size: 18px;
  font-weight: 500;
}
.askQuestion {
  padding: 70px 0px;
}

.questionItem {
  padding: 20px 10px 15px;
  background: white;
  box-shadow: 0 3px 12.35px 0.65px rgba(0, 0, 0, 0.1);
}
.answerItem {
  font-size: 18px;
}
.iconStyle {
  cursor: pointer;
}
</style>