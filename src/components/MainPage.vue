<template>
  <div>
    <div class="container main_background">
      <div class="row">
        <div class="col-md-6 main_page_left">
          <img src="/static/img/payment1.svg">
        </div>
        <div class="col-md-6 main_page_right">
          <h1 class="text-center rave_text">Welcome to RaveRide</h1>
          <p class="rave_text_p">Evie brings you the pages you'll need and the structure to create your own, with almost nothing to learn. It is minimal and mostly styles plain elements. There are only a few classes you'll need to know but nothing to disrupt your preferred coding style.</p>
          <div class="text-center"><a class="btn rave_button">Get Started</a></div>
        </div>
      </div>
    </div>

      <div class="container rave_ride_work">
        <div class="row">
          <div class="col-md-12">
            <p class="how_it_works">How RaveRide Works</p>
          </div>
          <div class="col-md-4 who">
            <img src="/static/img/request.svg">
            <h5 class="text-center rave_flow">Request for a ride</h5>
            <p class="rave_flow_text">A landing page for your open source projects. Present your solution, easily create docs.</p>
          </div>
          <div class="col-md-4 who">
            <img src="/static/img/ride.svg">
            <h5 class="text-center rave_flow">Move to your destination</h5>
            <p class="rave_flow_text">A landing page for your open source projects. Present your solution, easily create docs.</p>
          </div>
          <div class="col-md-4 who">
            <img src="/static/img/pay.svg">
            <h5 class="text-center rave_flow">Complete ride and pay</h5>
            <p class="rave_flow_text">A landing page for your open source projects. Present your solution, easily create docs.</p>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {};
  }
};
</script>

<style scoped>
.main_background{
  margin-top: 20px;
  margin-bottom: -100px;
}
.main_page_left img {
  height: 800px;
  width: 530px;
  margin-top: -170px;
}

.main_page_right {
  margin-top: 94px;
}

.rave_button{
  background-color: 	#6db052;
  color: #ffff!important;
}
.rave_text {
  color: 	#6db052;
  font-size: 40px;
  font-weight: 700;
  font-family: 'Acme', sans-serif;
}
/* .rave_text_p {
  font-family: 'Acme', sans-serif;
} */

.rave_flow{
  font-family: 'Acme', sans-serif;
  font-size: 20px;
  font-weight: 400;
}

.rave_flow_text{
  color: #666;
}

.rave_ride_work{
  margin-bottom: 40px;
}

.how_it_works {
  text-align: center;
  font-size: 30px;
  font-weight: 600;
  font-family: 'Acme', sans-serif;
  color: 	#6db052;
  padding-top: 20px;
}

.who img {
  width: 150px;
  height: 150px;
  margin: auto;
  display: block;
}

</style>
