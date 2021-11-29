<template>
  <footer>
    <div class="container">
      <div class="row p_70">
        <div class="sx col-6 fs_12 text-muted">
          <h5 class="fs-6 text-black fw-bold pb-3">Address</h5>
          <p>382 NE 191st St # 87394 Miami, FL 33179-3899</p>
          <p>+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)</p>
          <p>support@maxcoach.com</p>
          <span class="icons fs-3">
            <a href=""><i class="fab fa-facebook-square text-muted"></i></a>
            <a href=""><i class="fab fa-twitter ps-4 text-muted"></i></a>
            <a href=""><i class="fab fa-instagram ps-4 text-muted"></i></a>
            <a href=""><i class="fab fa-linkedin ps-4 text-muted"></i></a>
          </span>
        </div>
        <div class="col-6 dx d-flex">
          <div>
            <h5 class="fs-6 text-black fw-bold pb-3">Explore</h5>
            <div class="explore col-4 d-flex flex-column flex-wrap">
              <p class="fs_12" v-for="single in explore" :key="single.link">
                <a class="text-muted" href="">{{ single.link }}</a>
              </p>
            </div>
          </div>
          <div class="col-4 info">
            <h5 class="fs-6 text-black fw-bold pb-3">Information</h5>
            <p class="fs_12" v-for="single in info" :key="single.link">
              <a class="text-muted" href="">{{ single.link }}</a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      explore: [
        { link: "Start here" },
        { link: "Blog" },
        { link: "About us" },
        { link: "Success story" },
        { link: "Courses" },
        { link: "Contact us" },
      ],

      info: [
        { link: "Membership" },
        { link: "Purchase guide" },
        { link: "Private policy" },
        { link: "Terms of services" },
      ],
    };
  },
};
</script>

<style lang="scss">
footer {
  .container {
    .row {
      height: 180px;

      .sx {
        font-weight: 600;
      }

      .dx {
        h5 {
          width: 300px;
        }
        .explore {
          height: 130px;
        }
        p {
          width: 140px;
          a {
            text-decoration: none;
            font-weight: 600;
          }
        }
      }

      .info {
      }
    }
  }
}
</style>