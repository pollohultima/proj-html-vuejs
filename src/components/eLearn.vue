<template>
  <section class="e_learn mb_150">
    <!-- First item -->
    <div class="container mb_150">
      <div class="text-start d-flex">
        <!-- Side text section -->
        <div class="side_text col-5">
          <h6 class="fs_12 text-muted mb-4 fw-bold">
            WHY HESITATE TO REGISTER?
          </h6>
          <h1 class="mb-4 fw-bolder">
            Learn At Your Own <span class="fw-normal">Pace</span>
          </h1>

          <!-- Features List -->
          <ul class="list-group border-0 mb-4">
            <li class="list-group-item px-0">
              <i class="fas fa-check pe-3"></i> Select & customize courses to
              you preferences
            </li>
            <li class="list-group-item px-0">
              <i class="fas fa-check pe-3"></i> Change the tutor and make
              arrangements
            </li>
            <li class="list-group-item px-0">
              <i class="fas fa-check pe-3"></i> Partecipate in events to join
              others
            </li>
            <li class="list-group-item px-0">
              <i class="fas fa-check pe-3"></i> Get desired cretificate
              delivered at house
            </li>
          </ul>
          <a href="#" class="btn btn-link fs_12 fw-bold text-white p-0 border-0"
            >Get started for free</a
          >
        </div>

        <!-- Side image -->
        <div class="position-relative ms-4 ps-5">
          <img
            class="learn_guy position-relative"
            src="../assets/img/home-5-image-01.png"
            alt=""
          />
          <img
            class="grey_stain position-absolute translate-middle"
            src="../assets/img/underlay-shape-grey.svg"
            alt=""
          />
          <img
            class="mc_shape position-absolute translate-middle"
            src="../assets/img/maxcoach-shape-05.png"
            alt=""
          />
        </div>
      </div>
    </div>

    <!-- Second Item -->
    <div class="container">
      <div class="text-start d-flex align-items-center wrapper">
        <!-- Side image -->
        <div class="position-relative ps-5">
          <img
            class="learn_mobile position-relative"
            src="../assets/img/home-5-image-02.png"
            alt=""
          />
          <img
            class="grey_stain_2 position-absolute translate-middle"
            src="../assets/img/underlay-shape-grey.svg"
            alt=""
          />
          <img
            class="mc_shape_square position-absolute translate-middle"
            src="../assets/img/maxcoach-shape-07.png"
            alt=""
          />
          <img
            class="stripes position-absolute translate-middle"
            src="../assets/img/maxcoach-shape-01.png"
            alt=""
          />
          <div class="circle position-absolute"></div>
        </div>

        <!-- Side text section -->
        <div class="side_text col-6 ms_150">
          <h6 class="fs_12 text-muted mb-4 fw-bold">
            WHAT ARE YOU LOOKING FOR?
          </h6>
          <h1 class="mb-4 fw-bolder">
            Learn on you <span class="fw-normal">mobile</span> anytime!
          </h1>

          <!-- Features text -->
          <div class="text-muted pb-4">
            <p>
              Save lessons for later and revise or write notes at any time and
              on multiple devices on your way. Never interfere with activities
              of enjoyment or other precious moments.
            </p>
          </div>
          <a href="#" class="btn btn-link fs_12 fw-bold text-white p-0 border-0"
            >Get started for free</a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.e_learn {
  .learn_guy {
    z-index: 2;
  }

  .grey_stain {
    width: 430px;
    left: 180px !important;
    top: 350px;
    z-index: 1;
  }

  .mc_shape {
    right: -170px;
    bottom: -35px;
  }

  .wrapper {
    margin-left: 80px;

    .learn_mobile {
      z-index: 2;
    }

    .grey_stain_2 {
      width: 450px;
      left: 140px !important;
      top: 325px;
      z-index: 1;
    }

    .mc_shape_square {
      right: -190px;
      bottom: -35px;
    }

    .stripes {
      left: -110px;
      top: 255px;
    }

    .circle {
      right: -90px;
      top: 40px;
    }
  }

  h1 {
    color: $max_wine;
    padding-right: 100px;
  }
  span {
    color: $aquagreen;
  }
  .side_text {
    .list-group {
      .list-group-item {
        border: 0;
        i {
          color: $aquagreen;
          font-size: 1.2rem;
        }
      }
    }
    .btn {
      background: $aquagreen;
      width: 210px;
      line-height: 50px;
      text-decoration: none;
    }
  }
}
</style>