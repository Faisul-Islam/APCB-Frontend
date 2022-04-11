<template>
  <div class="container-md text-center mx-auto">
 <div v-if="!loading">
       <div class="content px-5 pb-2">
      <img
        src="@/assets/illustration-pc.svg"
        alt="PC"
        width="200"
        height="200"
      />
      <h1>Build your dream PC with just</h1>
      <h1><span class="secondary-color-text">One</span> click!</h1>
      <p class="p-2">
        Just provide your budget & we will make the decision for you.
      </p>
      <!--  -->
    </div>
    <div class="row g-3 justify-content-center">
      <div class="col-auto">
        <input
          type="number"
          class="form-control form-control-lg cstm-input-number"
          id="budget"
          placeholder="Budget"
          min="0"
          v-model="price"
        />
      </div>
      <div class="col-auto">
        <button class="btn btn-primary btn-lg mb-3" @click="loading = true; getPcBuild()">
          Build
        </button>
      </div>
    </div>
 </div>
    <apcb-loader v-if="loading"></apcb-loader>
  </div>
</template>

<script>
// @ is an alias to /src
/* eslint-disable */
import ApcbLoader from "@/components/ApcbLoader";
import axios from "axios";
export default {
  components: {
    ApcbLoader
  },
  data(){
    return {
      loading: false,
      price: 0,
    }
  },
  methods: {
    getPcBuild(){
      axios({
        method: "GET",
        url: `https://auto-pc-builder.herokuapp.com/apcb/get/b=amd&p=${this.price}`
      }).then(res => {
        console.log(res);
      }).catch(err => {

      }).finally(() => {

      });
    }
  }
};
</script>
<style>
/* .container-md{

} */
</style>
