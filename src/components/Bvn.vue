<template>
      <div>
    <div class="container main_background">
      <div class="row">
        <div class="col-md-6 main_page_left">
          <img src="/static/img/payment1.svg">
        </div>
        <div class="col-md-6 main_page_right">
            <h1 class="text-center rave_text">BVN Checker</h1>
            <p></p>
            <form @submit.prevent="verifyUser">
                <div class="form-group">
                <input type="number" class="form-control" placeholder="Please enter your BVN for verification" v-model="user.bvn"><br>
                <div class="text-center"><button :disabled="isDisabled" class="btn rave_button">Verify BVN</button></div>
                </div>
            </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
        user:{
            bvn: ""
        }
    };
  },

  computed:{
      isDisabled() {
      if (
        this.user.bvn
      ) {
        return false;
      } else {
        return true;
      }
    }
  },

  methods:{
      
    addUser() {
      let verifyUser = {
        bvn: this.user.bvn,

      };

      axios
        .get(" https://ravesandboxapi.flutterwave.com/v2/kyc/bvn/12345678901?seckey=FLWSECK-afef31fa991c36e4c82ecd0e520b6cd0-X \
 ", verifyUser)
        .then(res => {
          console.log(res.data);
        })
        .catch(err => {
          console.log(err);
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
