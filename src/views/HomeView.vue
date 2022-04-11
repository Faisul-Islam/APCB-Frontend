<template>
  <div class="container-md">
 <div class="text-center  mx-auto" v-if="!loading && response === undefined">
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
    <apcb-loader class="text-center  mx-auto" v-if="loading  && response === undefined"></apcb-loader>
    <components-list :response="response"  v-if="!loading  && response !== undefined"></components-list>
  </div>
</template>

<script>
// @ is an alias to /src
/* eslint-disable */
import ApcbLoader from "@/components/ApcbLoader";
import ComponentsList from "@/views/ComponentsList";
import axios from "axios";
export default {
  components: {
    ApcbLoader,
    ComponentsList
  },
  data(){
    return {
      loading: false,
      price: 0,
      response: undefined,
    }
  },
  methods: {
    getPcBuild(){
      axios({
        method: "GET",
        url: `https://auto-pc-builder.herokuapp.com/apcb/get/b=amd&p=${this.price}`
      }).then(res => {
        console.log(res);
        this.response = res.data;
      }).catch(err => {

      }).finally(() => {
       this.loading = false;
      });
    }
  }
};
</script>
<style>
/* .container-md{

} */
</style>
