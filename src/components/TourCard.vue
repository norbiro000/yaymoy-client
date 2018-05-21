<template>
  <div class="tour-card tour-card--border-rounded tour-card__theme-bright shadow-1">
    <img :src="image" alt="" class="tour-card__image ">
    <div class="tour-card__content">
      <h3 class="tour-card__category_text_display">{{ categoryName }}</h3>
      <h1 class="tour-card__title">{{ title }}</h1>
      <p class="tour-card__description">
        {{ shortDescription }}
      </p>

    </div>
  </div>
</template>

<script>
export default {
  props: {
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
    }
  }
}
</script>

<style scoped>
.tour-card {
  width: 100%;
  padding: 0px;
  margin: 40px auto;
  overflow: hidden;
  cursor: pointer;
}

.tour-card:first-child {
  margin: 0px auto;
}

.tour-card__content {
  padding: 0px 16px 32px 16px;
  font-weight: 300;
}

.tour-card--border-rounded {
  border-radius: 20px;
}
.tour-card__image {
  position: relative;
  width: 100%;
}

.tour-card__theme-bright {
  font-family: 'IBM Plex Sans';
}

.shadow-1 {
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.15);
}

.tour-card__price-banner {
  position: relative;
  top: 100%;
}

/* Text */
.tour-card__title {
  margin: 0px;
  font-weight: bold;
}
.tour-card__category_text_display {
  color:gray;
  margin: 0px;
  margin-top: 16px;
}
.tour-card__description {
  margin: 0px;
  margin-top: 8px;
  color:gray;
}
</style>
