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

        <!-- Side image -->
        <div
          class="
            maxcoach
            text-start
            d-flex
            align-items-center
            justify-content-between
          "
        >
          <img src="../assets/img/about-us-03-image-01.png" alt="" />

          <!-- Side text section -->
          <div class="side_text col-5">
            <h6 class="fs_12 text-muted mb-3">
              DREAM WITH <span class="fw-bolder">MAXCOACH</span>
            </h6>
            <h1 class="mb-4 fw-bolder">
              Construct A <span class="fw-normal">Stunning</span> Career
              Perspective
            </h1>
            <p class="mb-4">
              Learn any coding program in distance and for a reasonable fee. You
              don't have to struggle alone, you've got our assistance and help
            </p>
            <a class="btn p-0 border-0 text-center text-white fw-bold" href="#"
              ><i class="fas fa-download"></i> Download free E-book</a
            >
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
}
</style>