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

    <CodingCourse :featComp="features" />

    <!-- Banner with MaxCoach Data -->
    <DataBanner />

    <!-- Latest Courses section -->
    <LatestCourses :courseComp="courses" />

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
    <MaxEvents :eventsComp="events" />

    <!-- Past users feedbacks -->
    <Feedbacks :testimonialsComp="testimonials" />
  </main>
</template>

<script>
import CodingCourse from "./CodingCourse.vue";
import DataBanner from "./DataBanner.vue";
import LatestCourses from "./LatestCourses.vue";
import MaxEvents from "./MaxEvents.vue";
import Feedbacks from "./Feedbacks.vue";

export default {
  components: {
    CodingCourse,
    DataBanner,
    LatestCourses,
    MaxEvents,
    Feedbacks,
  },

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