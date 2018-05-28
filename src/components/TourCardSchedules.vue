<template>
<div class="schedules">
  <h2 class="schedules__title">
    Itinerary
  </h2>
  <div class="schedules__timeline">
    <div class="schedules__timeline__container"
      v-for="(schedule, index) in schedules"
      :key="schedule.title"
      :class="leftOrRight(index)"
      >
      <div class="schedules__timeline__content shadow-2">
        <b class="schedules__timeline__content__time">{{ schedule.time }}</b>
        <p class="schedules__timeline__content__description">{{ schedule.description }}</p>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  props: ['schedules'],
  methods: {
    leftOrRight (index) {
      return index % 2 === 0 ? 'left' : 'right'
    }
  }
}
</script>

<style lang="scss" scoped>
.schedules {
  margin: 32px 0px;

  /* The actual timeline (the vertical ruler) */
  &__timeline {
    position: relative;
    max-width: 100%;
    margin: 32px auto;

    &::after {
      content: '';
      position: absolute;
      width: 2px;
      background-color: gray;
      top: 0;
      bottom: 0;
      left: 50%;
      margin-left: -7px;
    }

    /* Container around content */
    &__container {
      padding: 10px 40px;
      position: relative;
      background-color: inherit;
      width: 50%;

      /* The circles on the timeline */
      &::after {
        content: '';
        position: absolute;
        width: 16px;
        height: 16px;
        right: -4px;
        background-color: white;
        border: 2px solid gray;
        top: 15px;
        border-radius: 50%;
        z-index: 1;
      }
    }

    /* The actual content */
    &__content {
      padding: 8px 16px;
      position: relative;
      border-radius: 6px;

      &__time {
        color: black;
      }

      &__description {
        color: gray;
        font-size: 13px;
      }
    }
  }
}
* {
  box-sizing: border-box;
}

/* Place the container to the left */
.left {
  left: 0;
}

/* Place the container to the right */
.right {
  left: 50%;
}

/* Add arrows to the left container (pointing right) */
.left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 16px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid white;
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent white;
}

/* Add arrows to the right container (pointing left) */
.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 16px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid white;
  border-width: 10px 10px 10px 0;
  border-color: transparent white transparent transparent;
}

/* Fix the circle for containers on the right side */
.right::after {
  left: -16px;
}

/* Media queries - Responsive timeline on screens less than 600px wide */
@media screen and (max-width: 600px) {
/* Place the timelime to the left */
  .schedules__timeline::after {
    left: 31px;
  }

/* Full-width containers */
  .schedules__timeline__container {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }

/* Make sure that all arrows are pointing leftwards */
  .schedules__timeline__container::before {
    left: 60px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
  }

/* Make sure all circles are at the same spot */
  .left::after, .right::after {
    left: 15px;
  }

/* Make all right containers behave like the left ones */
  .right {
    left: 0%;
  }
}
</style>
