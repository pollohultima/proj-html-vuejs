<template>
  <main class="position-relative">
    <div
      class="
        tools
        position-fixed
        d-flex
        flex-column
        justify-content-around
        align-items-center
      "
    >
      <i class="fas fa-ruler-combined"></i>
      <i class="far fa-life-ring"></i>
      <i class="fas fa-book"></i>
      <i class="fas fa-shopping-cart"></i>
    </div>
    <section class="coding_course">
      <div class="container text-center">
        <h6 class="fs_12 text-muted mb-3 fw-bold">
          START LEARNING CODING LANGUAGES
        </h6>
        <h1 class="mb_100 fw-bolder">
          Build Your Dream <span class="fw-normal">TODAY</span>
        </h1>

        <div class="coding_features d-flex justify-content-between mb_100">
          <div
            class="card col-3 border-0"
            v-for="feature in features"
            :key="feature.title"
          >
            <img
              :src="require(`../assets/img/${feature.img}`)"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body px-0">
              <h5 class="card-title mb-3">{{ feature.title }}</h5>
              <p class="card-text fs_14 text-muted">
                {{ feature.descr }}
              </p>
              <a
                href="#"
                class="btn btn-link fs_12 fw-bold text-muted"
                id="startNow"
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
          <div class="position-relative ps-5">
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
            <h6 class="fs_12 text-muted mb-4 fw-bold">
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

    <!-- Banner with MaxCoach Data -->
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

    <!-- Latest Courses section -->
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
            v-for="course in courses"
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

    <!-- E-learning features -->
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
            <a
              href="#"
              class="btn btn-link fs_12 fw-bold text-white p-0 border-0"
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
            <a
              href="#"
              class="btn btn-link fs_12 fw-bold text-white p-0 border-0"
              >Get started for free</a
            >
          </div>
        </div>
      </div>
    </section>

    <!-- Upcoming events -->
    <section class="events">
      <div class="bg pb_100">
        <div class="container">
          <div class="text-center">
            <h6 class="fs_12 text-muted mb-4 fw-bold">GET IN CONTACT NOW</h6>
            <h1 class="mb_70 fw-bolder">
              Upcoming <span class="fw-normal">Events</span>
            </h1>
          </div>

          <!-- Events list -->
          <div class="row justify-content-between m-0">
            <div
              class="
                event
                d-flex
                justify-content-between
                rounded
                position-relative
              "
              v-for="event in events"
              :key="event.id"
            >
              <div class="location">
                <p class="text-muted">
                  <i class="fas fa-map-marker-alt pe-2"></i>{{ event.location }}
                </p>
                <h5 class="fw-bold">{{ event.event_name }}</h5>
              </div>
              <div class="date d-flex flex-column align-items-center">
                <h2 class="day">{{ event.day }}</h2>
                <h6 class="month fw-bold">{{ event.month }}</h6>
                <a
                  href="#"
                  class="btn btn-link fs_12 fw-bold text-white py-1 border-0"
                  >Get tickets</a
                >
              </div>
              <div class="line position-absolute rounded"></div>
            </div>
          </div>
          <h6 class="fs_12 text-muted text-center mt-4 mb-4 fw-bold">
            Excited about our event?
            <span
              >View all event <i class="fas fa-long-arrow-alt-right"></i>
            </span>
          </h6>
        </div>
      </div>
    </section>

    <!-- Past users feedbacks -->
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
            v-for="testimonial in testimonials"
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
  </main>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          img: "home-5-image-box-01.png",
          title: "Idea Discussion",
          descr:
            "Get teamed up with the specialists who work and teach coding for years at famous universities.",
        },

        {
          img: "home-5-image-box-02.png",
          title: "Web Development",
          descr:
            "Learn to start nuilding a webpage from scratch. You decide your own pace, course and speed.",
        },

        {
          img: "home-5-image-box-03.png",
          title: "System Administration",
          descr:
            "Learners are encouraged to study the mechanism and structure of system administration.",
        },

        {
          img: "home-5-image-box-04.png",
          title: "Graphic Design",
          descr:
            "Have a passion fro graphic and arts? Show your talents with confidence and self-assertiveness.",
        },
      ],

      courses: [
        {
          id: "1",
          teacher_img: "73ee246daf47502812ccefc84bf02898.jpeg",
          teacher_name: "Blanche Fields",
          price: "$40.00",
          course_img: "course-02-480x298.jpg",
          course_name: "Learning to Write as a Professional Author",
          lessons: "20",
          students: "50",
        },

        {
          id: "2",
          teacher_img: "d0d504142acfde820eef2f11feea6253.jpeg",
          teacher_name: "Mary Strickland",
          price: "Free",
          course_img: "stock-full-hd-03-480x298.jpg",
          course_name: "Customer-centric Info-Tech Strategies",
          lessons: "24",
          students: "769",
        },

        {
          id: "3",
          teacher_img: "d0d504142acfde820eef2f11feea6253.jpeg",
          teacher_name: "Mary Strickland",
          price: "$19.00",
          course_img: "stock-full-hd-04-480x298.jpg",
          course_name: "Open Programming Courses for Everyone: Python",
          lessons: "17",
          students: "62",
        },

        {
          id: "4",
          teacher_img: "73ee246daf47502812ccefc84bf02898.jpeg",
          teacher_name: "Blanche Fields",
          price: "$26.00",
          course_img: "stock-full-hd-06-480x298.jpg",
          course_name: "Academic Listening and Note-taking",
          lessons: "14",
          students: "67",
        },

        {
          id: "5",
          teacher_img: "73ee246daf47502812ccefc84bf02898.jpeg",
          teacher_name: "Blanche Fields",
          price: "$39.00",
          course_img: "course-featured-image-01-480x298.jpg",
          course_name: "Master jQuery in a Shot Period of Time",
          lessons: "6",
          students: "51",
        },

        {
          id: "6",
          teacher_img: "73ee246daf47502812ccefc84bf02898.jpeg",
          teacher_name: "Blanche Fields",
          price: "$59.00",
          course_img: "course-02-480x298.jpg",
          course_name: "Master jQuery in a Shot Period of Time",
          lessons: "14",
          students: "76",
        },
      ],

      events: [
        {
          id: "1",
          location: "Texas, US",
          event_name: "Storytelling Workshop",
          day: "22",
          month: "NOV",
        },

        {
          id: "2",
          location: "New York, US",
          event_name: "Painting Art Contest 2020",
          day: "10",
          month: "OCT",
        },

        {
          id: "3",
          location: "Hamburg, Germany",
          event_name: "Storytelling Workshop",
          day: "23",
          month: "NOV",
        },

        {
          id: "4",
          location: "Illinois, US",
          event_name: "Street Performance: Call for Artist",
          day: "15",
          month: "DEC",
        },

        {
          id: "5",
          location: "llinois, US",
          event_name: "Consumer Food Safety Education Conference",
          day: "22",
          month: "JUL",
        },

        {
          id: "6",
          location: "Dubai",
          event_name: "How medation improve your mental health?",
          day: "12",
          month: "AUG",
        },
      ],

      testimonials: [
        {
          avatar: "testimonial-avata-02.jpg",
          message:
            "I am free to learn at my own pace, follow my own schedule and choose the subject I like. Great study portal for people like me.",
          name: "MINA HOLLACE",
          job: "/ Freelancer",
          id: "1",
        },

        {
          avatar: "testimonial-avata-04.jpg",
          message:
            "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
          name: "MADLEY PONDOR",
          job: "/ IT Specialist",
          id: "2",
        },

        {
          avatar: "testimonial-avata-01.jpg",
          message:
            "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.",
          name: "LUVIC DUBBLE",
          job: "/ Private Tutor",
          id: "3",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.tools {
  height: 160px;
  width: 40px;
  top: 200px;
  right: 0;
  background-color: #fff;
  border-top-left-radius: 5px !important;
  border-bottom-left-radius: 5px !important;
  z-index: 2;
}

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
      }
    }
  }

  .maxcoach {
    .about_us_3 {
      z-index: 2;
    }
    .purple_stain {
      width: 390px;
      left: 100px !important;
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

.events {
  h1 {
    color: $max_wine;
  }
  span {
    color: $aquagreen;
  }
  background: $event_bg;
  .bg {
    background: white;
    border-bottom-right-radius: 55% 40%;
  }

  .event {
    width: 570px;
    padding: 33px;
    margin-bottom: 30px;
    background: $event_bg;
    transition: all 0.5s;
    border: 3px transparent;

    &:hover {
      background: white;
      cursor: pointer;
      box-shadow: 0 0.5rem 1rem rgba(black, 0.15);
      border-left-color: 3px solid $aquagreen !important;
    }

    &:hover .line {
      opacity: 100%;
    }

    .day {
      color: $aquagreen;
    }
    .btn {
      background: $aquagreen;
      width: 130px;
      text-decoration: none;
    }

    .line {
      height: 100%;
      top: 0;
      left: 0;
      width: 3px;
      background-color: $aquagreen;
      opacity: 0%;
      transition: all 0.5s;
      border-top-right-radius: 0 !important;
      border-bottom-right-radius: 0 !important;
    }
  }

  h6 {
    span {
      border-bottom: 1px solid lightgray;
    }
  }
}

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