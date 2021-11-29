<template>
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
            v-for="event in eventsComp"
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
</template>

<script>
export default {
  props: {
    eventsComp: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

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
</style>