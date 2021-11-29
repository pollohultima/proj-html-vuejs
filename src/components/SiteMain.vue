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
    <eLearn />

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
import eLearn from "./eLearn.vue";

export default {
  components: {
    CodingCourse,
    DataBanner,
    LatestCourses,
    MaxEvents,
    Feedbacks,
    eLearn,
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
</style>