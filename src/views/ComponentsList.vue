<template>
  <div class="container-md">
      <list-item class="mb-2" :listData="response.cpu" title="CPU"></list-item>
      <list-item class="mb-2" :listData="response.mobo" title="Motherboard"></list-item>
      <list-item class="mb-2" :listData="response.ram" title="RAM"></list-item>
  </div>
</template>

<script>
import ListItem from "@/components/ListItem";
export default {
  props: ["response"],
  components: {
    ListItem
  },
  data(){
    return {

    }
  }

}
</script>

<style>

</style>