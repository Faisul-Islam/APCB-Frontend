<template>
  <div class="card">
    <div class="card-body list-item p-1">
      <div class="row">
        <div class="col-2">
          <img
            :src="listData.image"
            width="120px"
            class="img-fluid ml-2"
            :alt="title"
          />
        </div>
        <div class="col">
                <h4 class="main-color-text">
      <b>{{ title }}</b>
    </h4>
          <h5 class="card-title py-1">{{ listData.name }}</h5>
          <p class="card-text py-2">
            <b>{{ listData.price }}</b> ৳
          </p>
        </div>
      </div>
    </div>
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
</style>