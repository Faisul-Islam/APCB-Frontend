<template>
  <div class="pt-5 mt-5">
    <div class="lds-ripple">
      <div></div>
      <div></div>
    </div>
    <p class="pt-5">{{ qoute[idx] }}</p>
  </div>
</template>
<script>
import gsap from "gsap";
export default {
  data() {
    return {
      qoute: [
        "Please wait. We are building the best PC components for you.",
        "70% People ignore building a Desktop PC because of hassale choosing components",
        "A Desktop PC is faster than laptops",
        "Desktop PC can be upgraded later",
        "Desktop PC is best for professional works",
      ],
      idx: 0,
    };
  },
  methods: {
    startRandomQoutes() {
      setInterval(
        function () {
          this.idx < this.qoute.length - 1 ? (this.idx += 1) : (this.idx = 0);
         // console.log(this.idx);
        }.bind(this),
        4000
      );
    },
  },
  watch: {
    idx: function (val) {
      // this.idx = val;
       gsap.to(this.$data, { duration: 0.5, idx: val });
    },
  },
  mounted() {
    this.startRandomQoutes();
  },
};
</script>

<style scoped>
.lds-ripple {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
  transform: scale(2);
}
.lds-ripple div {
  position: absolute;
  border: 4px solid rgb(96, 47, 211);
  opacity: 1;
  border-radius: 50%;
  animation: lds-ripple 1s cubic-bezier(0, 0.2, 0.8, 1) infinite;
}
.lds-ripple div:nth-child(2) {
  animation-delay: -0.5s;
}
@keyframes lds-ripple {
  0% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 1;
  }
  100% {
    top: 0px;
    left: 0px;
    width: 72px;
    height: 72px;
    opacity: 0;
  }
}
</style>