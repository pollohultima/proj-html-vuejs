<template>
  <section class="feedback">
    <div class="container">
      <div class="text-center mb_150">
        <h6 class="fs_12 text-muted mb-4 fw-bold">
          PEOPLE ARE PRAISING MAXCOACH
        </h6>
        <h1 class="mb_70 fw-bolder">
          What make they <span class="fw-normal">love us?</span>
        </h1>
      </div>
      <div class="row justify-content-between">
        <div
          class="
            testimonial
            position-relative
            d-flex
            flex-column
            text-center
            rounded
          "
          v-for="testimonial in testimonialsComp"
          :key="testimonial.id"
        >
          <img
            class="
              rounded-circle
              position-absolute
              top-0
              start-50
              translate-middle
            "
            :src="require(`../assets/img/${testimonial.avatar}`)"
            alt=""
          />
          <p class="fb_text">
            {{ testimonial.message }}
          </p>
          <h5 class="fw-bold mb-4">{{ testimonial.name }}</h5>
          <p class="fs_14 text_muted">{{ testimonial.job }}</p>
        </div>
      </div>

      <div class="slider d-flex justify-content-between align-items-center">
        <div class="dot active"></div>
        <div class="dot unactive"></div>
        <div class="dot unactive"></div>
        <div class="dot unactive"></div>
      </div>

      <!-- Online certification banner -->
      <div class="cert text-center position-relative">
        <h4 class="fw-bold mb-2">
          Start today for getting
          <span class="fw-normal">Online Certification</span>
        </h4>
        <h2 class="fw-bold mb-5">
          You can be you own guiding star with our help!
        </h2>
        <a href="#" class="btn btn-link fs_12 fw-bold text-white p-0 border-0"
          >Get started now</a
        >
        <img
          class="position-absolute lines"
          src="../assets/img/maxcoach-shape-01.png"
          alt=""
        />
        <img
          class="position-absolute circle_shape"
          src="../assets/img/maxcoach-shape-02.png"
          alt=""
        />

        <div class="circle position-absolute"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    testimonialsComp: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.feedback {
  padding-top: 100px;
  border-top-right-radius: -50%;
  background: $event_bg;

  h1 {
    color: $max_wine;
  }

  span {
    color: $aquagreen;
  }

  .row {
    .testimonial {
      background: white;
      padding: 33px;
      width: 370px;
      height: 350px;

      img {
        width: 140px;
      }
      .fb_text {
        color: $max_wine;
        font-size: 16px;
        padding-top: 70px;
        margin-bottom: 40px;
        font-weight: 600;
      }
    }
  }

  .slider {
    width: 100px;
    margin: 50px auto;
    padding-bottom: 50px;

    .dot {
      width: 7px;
      height: 7px;
      background-color: gray;
      border-radius: 50%;
      border: none;
    }

    .active {
      width: 13px;
      height: 13px;
      background-color: $max_wine;
    }
  }

  .cert {
    h4,
    h2 {
      color: $max_wine;
    }

    padding-bottom: 100px;

    .btn {
      background: $aquagreen;
      width: 260px;
      line-height: 50px;
      text-decoration: none;
    }

    .circle_shape {
      bottom: 85px;
      right: 0px;
    }

    .lines {
      bottom: 165px;
      left: 0px;
    }

    .circle {
      left: 0px;
      top: 10px;
      border-color: #e6dcd2;
    }
  }
}
</style>