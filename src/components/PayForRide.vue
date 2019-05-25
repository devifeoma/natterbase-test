<template>
      <div>
    <div class="container main_background">
      <div class="row">
        <div class="col-md-6 main_page_left">
          <img src="/static/img/payment1.svg">
        </div>
        <div class="col-md-6 main_page_right">
            <h1 class="text-center rave_text">Pay for your ride</h1>
            <p></p>
            <form>
                <div class="form-group">
                <!-- <input type="number" class="form-control" placeholder="Please enter your BVN for verification" v-model="user.bvn"><br> -->
                <div class="text-center"><button class="btn rave_button" type="button" @click="payWithRave">Pay Now</button></div>
                </div>
            </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import axios from "axios";
export default {
  data() {
    return {
        API_publicKey:"FLWPUBK-ce3d36c1a0455318bc321fcf7829f94c-X"
    };
  },

  methods:{
        payWithRave() {
            var x = getpaidSetup({
                PBFPubKey: this.API_publicKey,
                customer_email: "user@example.com",
                amount: 2000,
                currency: "NGN",
                txref: "rave-123456",
                subaccounts: [
                {
                    id: "RS_1770B4221C5E9352F4BAD9ED1AA689A5"
                }
                ],
                meta: [{
                    metaname: "flightID",
                    metavalue: "AP1234"
                }],
                onclose: function() {},
                callback: function(response) {
                    var txref = response.tx.txRef; // collect flwRef returned and pass to a server page to complete status check.
                    console.log("This is the response returned after a charge", response);
                    if (
                        response.tx.chargeResponseCode == "00" ||
                        response.tx.chargeResponseCode == "0"
                    ) {
                        // redirect to a success page
                    } else {
                        // redirect to a failure page.
                    }

                    x.close(); // use this to close the modal immediately after payment.
                }
            });
        }
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
  margin-top: 150px;
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


.rave_flow_text{
  color: #666;
}
</style>
