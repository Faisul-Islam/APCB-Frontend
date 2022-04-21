<template>
  <div id="app">
    <!-- <d-card l="145px" t="320px" w="520px" h="520px"  d="120deg" class="asl"></d-card> -->
    <!-- <d-card l="185px" t="220px" w="40px" h="40px"></d-card>
    <d-card l="85px" t="270px" w="70px" h="70px"></d-card>
    <d-card l="255px" t="110px" w="85px" h="85px"></d-card>
    <d-card l="185px" t="300px" w="80px" h="80px"></d-card>
    <d-card l="475px" t="420px" w="60px" h="60px"></d-card>
    <d-card l="1305px" t="420px" w="76px" h="76px"></d-card>
    <d-card l="545px" t="156px" w="76px" h="76px"></d-card>
    <d-card l="445px" t="320px" w="60px" h="60px"></d-card>
    <d-card l="305px" t="520px" w="140px" h="140px"></d-card>
    <d-card l="405px" t="420px" w="76px" h="76px"></d-card> -->
    <!-- 
        <d-card l="145px" t="320px" w="120px" h="120px" d="120deg"></d-card>
    <d-card l="185px" t="220px" w="40px" h="65px" d="40deg"></d-card>
    <d-card l="85px" t="270px" w="70px" h="70px" d="160deg"></d-card>
    <d-card l="155px" t="110px" w="85px" h="65px" d="20deg"></d-card>
    <d-card l="185px" t="300px" w="80px" h="80px" d="140deg"></d-card>
    <d-card l="445px" t="420px" w="60px" h="60px" d="10deg"></d-card>
    <d-card l="1305px" t="420px" w="76px" h="180px" d="50deg"></d-card>
    <d-card l="445px" t="120px" w="76px" h="180px" d="50deg"></d-card>
    <d-card l="445px" t="320px" w="76px" h="60px" d="270deg"></d-card>
    <d-card l="385px" t="350px" w="76px" h="140px" d="150deg"></d-card>
    <d-card l="445px" t="420px" w="76px" h="80px" d="120deg"></d-card> -->
    <nav class="navbar navbar-expand-lg navbar-light p-3">
      <div class="container-fluid">
        <a class="navbar-brand" href=""
          ><img src="@/assets/logo.png" alt="APCB" width="60" height="60"
        /></a>
        <div class="" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link">About</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>
<script>
/* eslint-disable */
import DCard from "@/components/DCard";
export default {
  components: {
    DCard,
  },
};
</script>
<style>
.main-color-bg {
  background-color: #4c4086;
}
.secondary-color-bg {
  background-color: #f05760;
}

.main-color-text {
  color: #4c4086;
}
.secondary-color-text {
  color: #f05760;
}
/* .btn-primary {
  color: #fff;
  background-color: #4c4086;
  border-color: #4c4086;
}
.btn-primary:hover {
  color: #fff;
  background-color: #796db8;
  border-color: #796db8;
} */
.btn-primary{
      min-width: 138px;
    max-width: -webkit-fit-content;
    max-width: fit-content;
    max-width: -moz-fit-content;
    width: 100%;
    height: 50px;
    background: #7b68ee;
    border-radius: 8px;
    border: 1px solid #7b68ee;
    box-shadow: 0 10px 25px rgb(123 104 238 / 50%) !important;
}
.btn-primary:hover {
    background: #5c4dbc;
    border: 1px solid #5c4dbc;
}
#app {
  font-family: "Inter", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  position: relative;
  /* background: linear-gradient(to right,#acb6e5,#86fde8); */
  /* background: linear-gradient(to right, #d3cce3, #e9e4f0); */
  background: linear-gradient(to right, #e1dfe6, #f2eef8);
  height: 100vh;
  /* background-image: url("https://tailwindcss.com/_next/static/media/hero@75.4dea7abe609fc522c039fba7662ceea2.jpg");
      
      background-repeat: no-repeat;
  background-size: cover; */
}
h1 {
  font-weight: 800;
}
.cstm-input-number {
  background: rgba(255, 255, 255, 0.4);
  border-radius: 8px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
   /* box-shadow: 0 10px 25px rgb(123 104 238 / 50%) !important; */
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
}
.cstm-input-number:focus {
  background: rgba(255, 255, 255, 0.863);
  border-color: 1px solid rgba(255, 255, 255, 0.3) !important;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
}
/* .d-card{
  position: absolute;

background: rgba(255, 255, 255, 0.21);
border-radius: 16px;
box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
backdrop-filter: blur(5px);
-webkit-backdrop-filter: blur(5px);
border: 1px solid rgba(255, 255, 255, 0.89);
} */
.dc-1 {
  width: 120px;
  height: 120px;
  left: 10vw;
  transform: rotate(120deg);
}
.dc-2 {
  width: 78px;
  height: 190px;
  left: 10vw;
  top: 15vh;
  transform: rotate(65deg);
}
.dc-3 {
}
.dc-4 {
}
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type="number"] {
  -moz-appearance: textfield;
}
.container-fluid{
    z-index: 1 ;
}
</style>
