<template>
  <div class="card">
      <a :href="listData.link" target="_blank" rel="noopener noreferrer">
    <div class="card-body list-item p-2">
      <div class="row">
        <div class="col-4 col-md-2">
          <img
            :src="listData.image"
            width="120px"
            class="img-fluid"
            :alt="title"
          />
        </div>
        <div class="col">
                <h4 class="main-color-text">
      <b>{{ title }}</b>
    </h4>
          <h5 class="card-title py-1">{{ listData.name }}</h5>
          <p class="card-text py-0 py-md-2">
            <b>{{ listData.price }}</b> ৳
          </p>
        </div>
      </div>
    </div>
    </a>
  </div>
</template>

<script>
export default {
  props: ["listData", "title"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.list-item{
    transition: all 0.25s ease-in-out;
}
.list-item:hover{
    background-color:#e9e9e9;
    cursor: pointer;
}
a{
    color: black;
}
a:link { text-decoration: none; }


a:visited { text-decoration: none; }


a:hover { text-decoration: none; }


a:active { text-decoration: none; }
</style>