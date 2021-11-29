<template>
  <header>
    <!-- Navigator -->
    <div class="navigator">
      <div class="container d-flex align-items-center justify-content-between">
        <!-- Logo -->
        <div class="logo">
          <img src="../assets/img/dark-logo.png" alt="" />
        </div>

        <!-- All tabs and searchbar -->
        <div
          class="
            nav_search
            col-8
            d-flex
            align-items-center
            justify-content-between
          "
        >
          <a href="" v-for="tab in tabs" :key="tab.link"
            >{{ tab.link }} <i class="fas fa-chevron-down"></i
          ></a>
          <a href="" class="position-relative"
            >Shop <i class="fas fa-chevron-down"></i
            ><span
              class="
                position-absolute
                top-0
                start-100
                translate-middle
                badge
                rounded-circle
              "
              >0</span
            >
            <i class="fas fa-shopping-cart ps-2 text-black"></i
          ></a>
          <a href=""><i class="far fa-user-circle text-black"></i></a>

          <!-- Text input -->
          <div class="searchbox input-group d-flex align-items-center p-0">
            <input
              type="text"
              class="form-control srch border-end-0"
              placeholder="Search"
              aria-label="search"
              aria-describedby="basic-addon2"
              style="height: 100%"
            />
            <span class="input-group-text srch bg-white border-start-0"
              ><i class="fas fa-search"></i
            ></span>
          </div>
        </div>
      </div>
    </div>

    <!-- Header Jumbo -->
    <div class="jumbo position-relative">
      <div class="container d-flex justify-content-between align-items-center">
        <div class="side_text col-4 mb-3">
          <h1 class="mb-4 fw-bolder">
            Complete Your Dreams in Javas Programming
          </h1>
          <p class="mb-4">
            Learn any coding program in distance and for a reasonable fee. You
            don't have to struggle alone, you've got our assistance and help
          </p>
          <a class="btn p-0 border-0 text-center text-white fw-bold" href="#"
            ><i class="fas fa-download"></i> Download free E-book</a
          >
        </div>

        <div class="hero_image">
          <img
            class="img-fluid"
            src="../assets/img/home-5-hero-image.png"
            alt=""
          />
        </div>
      </div>

      <img
        class="jumbo_overlay position-absolute"
        src="../assets/img/jumbo-overlay.svg"
        alt=""
      />
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      tabs: [
        { link: "Home" },
        { link: "Pages" },
        { link: "Courses" },
        { link: "Features" },
        { link: "Blog" },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
header {
  height: 800px;
  background: $header_bg;

  .navigator {
    .container {
      height: 80px;
    }
    img {
      height: 25px;
    }
    .badge {
      background-color: $aquagreen;
      padding: 0 3.5px;
      line-height: 15px;
    }
    .nav_search {
      a {
        text-decoration: none;
        color: $max_wine;
        .fa-chevron-down {
          font-size: 8px;
          vertical-align: middle;
        }
      }
      .searchbox {
        width: 200px;
        i {
          color: $aquagreen;
        }
        .srch {
          height: 48px !important;
        }
      }
    }
  }

  .jumbo {
    .container {
      height: 720px;
      h1 {
        color: $max_wine;
      }
      .btn {
        background: $max_wine;
        line-height: 50px;
        vertical-align: middle;
        width: 260px;
        font-size: 14px;
      }
      .hero_image {
        z-index: 2;
        position: relative;
      }
    }
    .jumbo_overlay {
      width: 100%;
      height: 450px;
      bottom: 0px;
      transform: rotateY(180deg);
      z-index: 1;
    }
  }
}
</style>