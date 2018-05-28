<template>
  <transition>
    <div class="tour-display">
      <img :src="image" v-if="1==1">
      <div v-else class="show-no-image">
        <i class="far fa-images"></i>
      </div>
      <button class="button-close keep-right" @click="closePage"><i class="far fa-times"></i></button>

      <div class="tour-display__content">
        <h3 class="tour-display__category_text_display">{{ categoryName }}</h3>
        <h1 class="tour-display__title">{{ title }}</h1>
        <p class="tour-display__description">
          {{ description }}
        </p>
        <hr/>
        <div class="tour-display__schedule">
          <TourCardSchedules
            :schedules="schedules"
            >
          </TourCardSchedules>
        </div>
        <hr/>
      </div>
    </div>
  </transition>
</template>

<script>
import TourCardSchedules from './TourCardSchedules'
export default {
  props: {
    id: {
      type: String
    },
    title: {
      type: String,
      required: true,
      validator: function (value) {
        return [
          'syncing',
          'synced',
          'version-conflict',
          'error'
        ].indexOf(value) !== -1
      }
    },
    image: {
      type: String
    },
    categoryName: {
      type: String
    },
    shortDescription: {
      type: String
    },
    description: {
      type: String
    },
    schedules: {
      type: Object
    }
  },
  methods: {
    closePage () {
      this.$router.go(-1)
    }
  },
  components: {
    TourCardSchedules
  }
}
</script>

<style lang="scss">
.tour-display {
  position: absolute;
  min-width: 100%;
  min-height: 100%;
  top: 0%;
  left: 0%;

  & img {
    width: 100%;
  }

  &__content {
    padding: 0px 16px 32px 16px;
    font-weight: 300;
  }

  &__title {
    margin: 0px;
    font-weight: bold;
  }

  &__category_text_display {
    color:gray;
    margin: 0px;
    margin-top: 16px;
  }
  &__description {
    margin: 0px;
    margin-top: 8px;
    color:gray;
  }
}

.keep-right {
  position: fixed;
  top: 16px;
  right: 16px;
}

.show-no-image {
  width: 100%;
  background: gray;
  height: 300px;
  text-align: center;

  & i {
    position: relative;
    color: white;
    font-size: 5rem;
    top: 50%;
    transform: translateY(-50%)
  }
}

hr {
  margin: 30px 0px;
  border: rgba($color: #000000, $alpha: 0.1) dashed 1px;
}
</style>
