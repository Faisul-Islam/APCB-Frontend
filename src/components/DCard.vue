// Author: Faisl islam
<template>
  <div
    class="dc-body"
    v-bind:style="{
      left: l,
      top: t,
      width: w,
      height: h,
      transform: 'rotate(' + d + ')',
    }"
  ></div>
</template>

<script>
export default {
  props: ["l", "t", "w", "h", "d"],
  data() {
    return {};
  },
};
</script>

<style>
.dc-body {
  position: absolute;
  background: rgba(255, 255, 255, 0.09);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.61);
  z-index: 0 ;
}
</style>