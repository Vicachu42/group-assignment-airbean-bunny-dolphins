<template>
  <div class="front-wrapper">
    <img
      class="intro-graphic-left"
      src="../assets/graphics/intro-graphic-left.svg"
      alt=""
    />
    <img
      class="intro-graphic-right"
      src="../assets/graphics/intro-graphic-right.svg"
      alt=""
    />
    <img
      class="airbean-landing"
      src="../assets/graphics/airbean-landing.svg"
      alt=""
    />
  </div>
</template>

<script>
export default {
  name: "Landing",
  created(){
    setTimeout(() => {
      this.$router.push("/menu");
    }, 5000);
  },
};
</script>

<style scoped>
body {
  display: flex;
  justify-content: center;
  align-items: center;
}
.front-wrapper {
  width: 375px;
  height: 667px;
  background: #38846d;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  position: relative;
}
.intro-graphic-left {
  margin-right: auto;
}
.intro-graphic-right {
  margin-left: auto;
}
.airbean-landing {
  position: absolute;
  top: 40%;
  bottom: 60%;
  margin-right: auto;
}
</style>
