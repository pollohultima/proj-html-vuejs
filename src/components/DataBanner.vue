<template>
  <div class="data_banner mb_100">
    <div class="container d-flex align-items-center">
      <div class="col-3 text-center fw-bold">
        <h1 class="mb-3 fw-bold">1.926</h1>
        <p>FINISHED SESSIONS</p>
      </div>

      <div class="col-3 text-center fw-bold">
        <h1 class="mb-3 fw-bold">3.092+</h1>
        <p>ENROLLED LEARNERS</p>
      </div>

      <div class="col-3 text-center fw-bold">
        <h1 class="mb-3 fw-bold">200</h1>
        <p>ONLINE INSTRUCTORS</p>
      </div>

      <div class="col-3 text-center fw-bold">
        <h1 class="mb-3 fw-bold">100%</h1>
        <p>SATISFACTION RATE</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.data_banner {
  height: 230px;
  background: #faf8f6;
  .container {
    height: 100%;
    h1 {
      color: $aquagreen;
    }
    p {
      color: $max_wine;
    }
  }
}
</style>