<template>
  <header>
    <div class="container">
      <div class="navigator d-flex align-items-center justify-content-between">
        <div class="logo">
          <img src="../assets/img/dark-logo.png" alt="" />
        </div>
        <div
          class="
            nav_search
            col-8
            d-flex
            align-items-center
            justify-content-between
          "
        >
          <a href="">Home <i class="fas fa-chevron-down"></i></a>
          <a href="">Pages <i class="fas fa-chevron-down"></i></a>
          <a href="">Courses <i class="fas fa-chevron-down"></i></a>
          <a href="">Features <i class="fas fa-chevron-down"></i></a>
          <a href="">Blog <i class="fas fa-chevron-down"></i></a>
          <a href=""
            >Shop <i class="fas fa-chevron-down"></i>
            <i class="fas fa-shopping-cart ps-2 text-black"></i
          ></a>
          <a href=""><i class="far fa-user-circle text-black"></i></a>

          <div class="searchbox input-group d-flex align-items-center p-1">
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
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
header {
  height: 800px;
  background: $header_bg;

  .navigator {
    height: 80px;
    img {
      height: 25px;
    }
    .nav_search {
      a {
        text-decoration: none;
        color: $header_font_color;
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
}
</style>