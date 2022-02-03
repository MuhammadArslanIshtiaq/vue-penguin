<template>
  <div>
    <b-jumbotron class="jumbotron"></b-jumbotron>
    <b-container class="bv-example-row fluid">
      <b-row>
         <b-col class="text-center" cols="3"></b-col>
        <b-col class="text-center" cols="3">
          <img src="getting_started.png" class="img-responsive  img-size"
        /></b-col>
        <b-col class="text-center" cols="3">
          <img src="getting_started.png" class="img-responsive  img-size"
        /></b-col>
      </b-row>
    </b-container>
  </div>
</template>
<style>
.jumbotron {
  background: url("../static/banner.jpg") no-repeat;
  background-size: cover;
  background-position: center center;
  vertical-align: middle;
  content: "";
  height: 90vh;
}
.center {
  display: flex;
  justify-content: center;
  text-align: center;
  margin-top: -10vh;
}
.row {
  margin-right: 0px !important;
  margin-left: 0px !important;
}
.img-size {
  position: relative;
  margin-top: -6vw;
  width: 60%;
}

@media screen and (max-width: 768px) {
  .img-size {
    width: 100%;
    margin-top: -23vw;
  }
}
</style>
<script>
export default {
  name: "HeroSection",
};
</script>
