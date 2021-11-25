<template>
  <main>
    <section class="coding_course">
      <div class="container text-center">
        <h6 class="fs_12 text-muted mb-3">START LEARNING CODING LANGUAGES</h6>
        <h1 class="mb_100 fw-bolder">
          Build Your Dream <span class="fw-normal">TODAY</span>
        </h1>

        <div class="coding_features d-flex justify-content-between mb_100">
          <div class="card col-3 border-0">
            <img
              src="../assets/img/home-5-image-box-01.png"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body px-0">
              <h5 class="card-title mb-3">Idea Discussion</h5>
              <p class="card-text fs_14 text-muted">
                Get teamed up with the specialists who work and teach coding for
                years at famous universities.
              </p>
              <a href="#" class="btn btn-link fs_12 fw-bold"
                >Start now <i class="fas fa-long-arrow-alt-right"></i
              ></a>
            </div>
          </div>
          <div class="card col-3 border-0">
            <img
              src="../assets/img/home-5-image-box-02.png"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body px-0">
              <h5 class="card-title mb-3">Web Development</h5>
              <p class="card-text fs_14 text-muted">
                Learn to start nuilding a webpage from scratch. You decide your
                own pace, course and speed.
              </p>
              <a href="#" class="btn btn-link fs_12 fw-bold"
                >Start now <i class="fas fa-long-arrow-alt-right"></i
              ></a>
            </div>
          </div>
          <div class="card col-3 border-0">
            <img
              src="../assets/img/home-5-image-box-03.png"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body px-0">
              <h5 class="card-title mb-3">System Administration</h5>
              <p class="card-text fs_14 text-muted">
                Learners are encouraged to study the mechanism and structure of
                system administration.
              </p>
              <a href="#" class="btn btn-link fs_12 fw-bold"
                >Start now <i class="fas fa-long-arrow-alt-right"></i
              ></a>
            </div>
          </div>
          <div class="card col-3 border-0">
            <img
              src="../assets/img/home-5-image-box-04.png"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body px-0">
              <h5 class="card-title mb-3">Graphic Design</h5>
              <p class="card-text fs_14 text-muted">
                Have a passion fro graphic and arts? Show your talents with
                confidence and self-assertiveness.
              </p>
              <a href="#" class="btn btn-link fs_12 fw-bold"
                >Start now <i class="fas fa-long-arrow-alt-right"></i
              ></a>
            </div>
          </div>
        </div>

        <!-- MaxCoach "Dream" -->
        <div
          class="
            maxcoach
            text-start
            d-flex
            align-items-center
            justify-content-between
          "
        >
          <!-- Side image -->
          <div class="position-relative">
            <img
              class="about_us_3 position-relative"
              src="../assets/img/about-us-03-image-01.png"
              alt=""
            />
            <img
              class="purple_stain position-absolute translate-middle"
              src="../assets/img/underlay-shape-lilla.svg"
              alt=""
            />
          </div>

          <!-- Side text section -->
          <div class="side_text col-6">
            <h6 class="fs_12 text-muted mb-4">
              DREAM WITH <span class="fw-bolder">MAXCOACH</span>
            </h6>
            <h1 class="mb-5 fw-bolder">
              Construct A <span class="fw-normal">Stunning</span> Career
              Perspective
            </h1>

            <!-- Side cards with header title -->
            <div class="card shadow mb-4">
              <h6
                class="
                  card-header
                  fw-bold
                  text-white
                  py-3
                  d-flex
                  justify-content-between
                  active
                "
              >
                <span
                  >Multiple Platforms Supported for Teaching & Studying
                </span>
                <span><i class="fas fa-minus-circle fs-6"></i> </span>
              </h6>
              <div class="card-body p-4">
                <p class="card-text text-muted">
                  MaxCoach supports the act of teaching and learning on multiple
                  platforms like online or offline via material downloads. We
                  know things aren't supposed to be devoured in a short time,
                  you can always acces our knowledge base from any device.
                </p>
              </div>
            </div>

            <div class="card shadow mb-4">
              <h6
                class="
                  card-header
                  fw-bold
                  text-muted
                  bg-white
                  py-3
                  d-flex
                  justify-content-between
                "
              >
                <span>Multiple Course Partecipation at the Same Time</span>
                <span><i class="fas fa-plus-circle fs-6"></i> </span>
              </h6>
            </div>

            <div class="card shadow mb-4">
              <h6
                class="
                  card-header
                  fw-bold
                  text-muted
                  bg-white
                  py-3
                  d-flex
                  justify-content-between
                "
              >
                <span>Track Study Progress & Deliver Prompt Feedback</span>
                <span><i class="fas fa-plus-circle fs-6"></i> </span>
              </h6>
            </div>
          </div>
        </div>
      </div>
    </section>

    <div class="data_banner">
      <div class="container"></div>
    </div>

    <section class="last_courses"></section>

    <section class="e_learn"></section>

    <section class="events"></section>

    <section class="feedback"></section>
  </main>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.coding_course {
  padding: 90px 0;

  h1 {
    color: $max_wine;
    span {
      color: $aquagreen;
    }
  }
  .card {
    img {
      width: auto;
      height: 175px;
      margin: auto;
    }
    .card-body {
      .btn {
        text-decoration: none;
        color: $max_wine;
      }
    }
  }

  .maxcoach {
    .about_us_3 {
      z-index: 2;
    }
    .purple_stain {
      width: 390px;
      left: 50px !important;
      top: 295px;
      z-index: 1;
    }
    .card {
      .active {
        background: $lightaquagreen;
      }
    }
  }
}
</style>