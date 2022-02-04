<template>
  <div>
    <b-jumbotron class="jumbotron"></b-jumbotron>
    <b-container class="bv-example-row fluid center">
      <b-row>
        <b-col class="text-center mb-5 mt-5" sm="12" md="6">
          <img src="getting_started.png" class="img-responsive img-size" />
        </b-col>
        <b-col class="text-center mt-5 mb-5" sm="12" md="6">
          <img src="White_Paper.png" class="img-responsive img-size" />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<style>
.jumbotron {
  background: url("../static/bg.jpg") no-repeat;
  background-size: cover;
  background-position: center center;
  vertical-align: middle;
  content: "";
  height: 100vh;
  border-radius: unset;
}
.center {
  display: flex;
  justify-content: center;
  text-align: center;
  margin-top: -25vh;
}
.row {
  margin-right: 0px !important;
  margin-left: 0px !important;
}
.img-size {
  position: relative;
  margin-top: -6vw;
  width: 50%;
}

@media screen and (max-width: 768px) {
  .img-size {
    width: 70%;
    margin-top: -23vw;
  }
}
</style>
<script>
export default {
  name: "HeroSection",
};
</script>
