<template>
  <section class="last_courses pb_100 mb_100">
    <h6 class="fs_12 text-muted mb-3 text-center fw-bold">
      CHOOSE WHERE YOU'D LIKE TO BEGIN
    </h6>

    <h1 class="mb_50 fw-bolder text-center">
      Latest Featured <span class="fw-normal">Courses</span>
    </h1>

    <div class="container">
      <div class="row mb-5 justify-content-between gy-5">
        <div
          class="card position-relative border-0 p-0"
          v-for="course in courseComp"
          :key="course.id"
        >
          <div class="img_wrapper">
            <img
              :src="require(`../assets/img/${course.course_img}`)"
              class="card-img-top rounded-top"
              alt="..."
            />
          </div>

          <div class="price position-absolute top-0 end-0 rounded">
            <h5 class="m-0 text-white fw-bold p-2">{{ course.price }}</h5>
          </div>
          <div class="card-body p-3">
            <div class="card-text fs_14 text-muted mb-3">
              <img
                class="rounded-circle"
                :src="require(`../assets/img/${course.teacher_img}`)"
                alt=""
              />
              <span class="text-muted ps-3">{{ course.teacher_name }}</span>
            </div>

            <h5 class="card-title fw-bold mb-4">
              {{ course.course_name }}
            </h5>

            <span class="card-text fs_14">
              <span class="text-muted"
                ><i class="far fa-file-alt"></i>
                {{ course.lessons }} Lessons</span
              >
              <span class="ms-4 text-muted"
                ><i class="far fa-user text-muted"></i>
                {{ course.students }} Students</span
              >
            </span>
          </div>
        </div>
      </div>
      <div class="row justify-content-center">
        <a href="#" class="btn btn-link fs_12 fw-bold text-white p-0 border-0"
          >View all courses <i class="fas fa-long-arrow-alt-right"></i
        ></a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    courseComp: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.last_courses {
  height: 100%;
  border-bottom-left-radius: 35% 10%;
  border-bottom-right-radius: 35% 10%;
  background-image: linear-gradient(white, #f5f5f5);

  h1 {
    color: $max_wine;
  }
  span {
    color: $aquagreen;
  }
  .card {
    width: 370px;
    background: transparent !important;
    transition: all 0.5s;
    overflow: hidden;

    .card-img-top {
      transition: all 0.5s;
    }

    &:hover {
      background: white !important;
      box-shadow: 0 0.5rem 1rem rgba(black, 0.15);
      cursor: pointer;
    }

    &:hover .card-img-top {
      transform: scale(1.1);
      object-fit: cover;
    }
    .img_wrapper {
      overflow: hidden;
    }

    .price {
      background: $aquagreen;
      border-top-left-radius: 0 !important;
      border-bottom-right-radius: 0 !important;
    }
  }

  .btn {
    background: $aquagreen;
    width: 260px;
    line-height: 50px;
    text-decoration: none;
  }
}
</style>