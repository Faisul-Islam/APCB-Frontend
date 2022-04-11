<template>
  <div id="app">
<nav class="navbar navbar-expand-lg navbar-light p-3">
  <div class="container-fluid">
    <a class="navbar-brand" href=""><img src="@/assets/logo.png" alt="APCB" width="60" height="60"></a>
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

<style>
.main-color-bg{
  background-color:#4c4086;

}
.secondary-color-bg{
  background-color:#f05760;

}

.main-color-text{
  color:#4c4086;
}
.secondary-color-text{
  color:#f05760;
}
.btn-primary {
    color: #fff;
    background-color: #4c4086;
    border-color: #4c4086;
}
.btn-primary:hover {
    color: #fff;
    background-color: #796db8;
    border-color: #796db8;
}
#app {
  font-family: 'Inter', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
      /* background-image: url("https://tailwindcss.com/_next/static/media/hero@75.4dea7abe609fc522c039fba7662ceea2.jpg");
      background-repeat: no-repeat;
  background-size: cover; */
}
h1{
  font-weight: 800 ;
}
.cstm-input-number{
 background-color: #edf2f7;
 border: 1px solid #dddee5;

}
.cstm-input-number:focus{
   background-color: white;
  border-color: #5c5194 !important;
      box-shadow: 0 0 0 0.25rem rgb(83 73 152 / 25%)
}
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type=number] {
  -moz-appearance: textfield;
}
</style>
