<template>
  <div>
    <div class="heroBgImage">
      <b-container fluid="sm">
        <div class="heroContent">
          <div>
            <div class="heroHeading">
              <h1>Get a website for your business</h1>
              <h2>
                Starting at
                <span class="labelPrice badge">$399</span>
              </h2>
              <div class="text-center pt-5">
                <b-button variant="outline" class="getBtn"
                  >Get Started</b-button
                >
              </div>
            </div>
          </div>
        </div>
      </b-container>
    </div>
  </div>
</template>  

<script type="text/javascript">
// import heroImage from "@/assets/images/Abstract-Envelope.svg";
export default {
  data: () => ({
    // heroImage: heroImage,
  }),
};
</script>

<style  scoped>
.heroContent {
  padding-top: 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80vh;
}
.heroHeading h1 {
  font-size: 2rem;
  font-weight: 500;
  line-height: 1.3em;
  text-align: center;
  color: white;
  text-align: center;
}
.heroHeading h2 {
  font-size: 3rem;
  font-weight: 500;
  line-height: 1.35em;
  text-align: center;
  color: white;
}

.labelPrice {
  background: rgba(20, 39, 78, 0.63137);
  font-size: 3.5rem;
}
.heroHeading {
  text-align: center;
  margin: 0 auto;
  color: white;
  position: relative;
}

.heroHeading p {
  font-size: 28px;
  line-height: 36px;
  font-weight: 500;
}
.getBtn {
  font-size: 1.4rem;
  padding: 0.6rem 1.3rem;
  font-weight: 600;
  border: 1px solid #ff5722;
  color: white;
  background: #ff5722;
  /* box-shadow: 0px 0px 10px 0px rgb(7 109 109 / 50%); */
}
.getBtn:hover {
  background: #14274e;
  color: #ff5722;
  border: 1px solid #14274e;
}

@media screen and (min-width: 576px) {
  .heroContent {
    padding-top: 2rem;
  }
  .heroHeading h1 {
    font-size: 2.5rem;
  }
  .heroHeading h2 {
    font-size: 3.5rem;
  }
  .labelPrice {
    font-size: 4rem;
  }
}

@media screen and (min-width: 768px){
 
}

@media screen and (min-width: 992px){
   .heroHeading h1 {
    font-size: 2.5rem;
  }
  .heroHeading h2 {
    font-size: 3.5rem;
  }
  .labelPrice {
    font-size: 4rem;
  }
}

@media screen and (min-width: 1200px){

}
</style>