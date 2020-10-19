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
                <span class="labelPrice badge ">$399</span>
              </h2>
              <div class="text-center pt-5">
                <b-button variant="outline" class="getBtn">Get Started</b-button>
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
  padding: 180px 0px 90px 0px;
}
.labelPrice {
  background: #14274ea1;
  font-size: 50px;
}
.heroHeading {
  width: 650px;
  text-align: center;
  margin: 0 auto;
  color: white;
  position: relative;
}
.heroHeading h1 {
  font-size: 2.5rem;
  font-weight: 500;
  line-height: 1.3em;
  text-align: center;
  color: white;
  text-align: center;
}
.heroHeading h2 {
  font-size: 3.5rem;
  font-weight: 500;
  line-height: 1.35em;
  text-align: center;
  color: white;
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
.getBtn:hover{
  background:#14274e;
  color:#ff5722;
   border: 1px solid #14274e;
}
</style>