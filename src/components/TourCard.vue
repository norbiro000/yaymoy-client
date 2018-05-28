<template>
  <transition name="menu-popover">
    <div class="tour-card tour-card--border-rounded tour-card__theme-bright shadow-1" @click="fullScreen">
      <img :src="image" alt="" class="tour-card__image ">
      <div class="tour-card__content">
        <h3 class="tour-card__category_text_display">{{ categoryName }}</h3>
        <h1 class="tour-card__title">{{ title }}</h1>
        <p class="tour-card__description">
          {{ shortDescription }}
        </p>
      </div>
    </div>
    </transition>
</template>

<script>
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
    fullScreen () {
      let props = {
        image: this.image,
        title: this.title,
        id: this.id,
        categoryName: this.categoryName,
        shortDescription: this.shortDescription,
        description: this.description,
        schedules: this.schedules
      }
      this.$router.push({name: 'tour', params: props})
    }
  }
}
</script>

<style lang="scss" scoped>
div {
  transition: all 200ms;
}

.tour-card {
  position: relative;
  width: 100%;
  padding: 0px;
  margin: 40px auto;
  overflow: hidden;
  cursor: pointer;
  background: white;

  &:first-child {
    margin: 0px auto;
  }

  &__content {
    padding: 0px 16px 32px 16px;
    font-weight: 300;
  }

  &__image {
    position: relative;
    width: 100%;
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

  &__theme-bright {
    font-family: 'IBM Plex Sans';
  }

  &--border-rounded {
    border-radius: 20px;
  }
}
</style>
