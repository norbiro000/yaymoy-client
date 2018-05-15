<template>
  <div id="app" class="">
    <h1 class="app-title">YaymoY</h1>
    <TourCardView>
      <TourCard></TourCard>
      <TourCard></TourCard>
      <TourCard></TourCard>
      <TourCard></TourCard>
      <TourCard></TourCard>
      <TourCard></TourCard>
    </TourCardView>
  </div>
</template>

<script>
import TourCard from '@/components/TourCard'
import TourCardView from '@/components/TourCardView'
export default {
  components: {
    TourCard,
    TourCardView
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=IBM+Plex+Sans|Pacifico');
body, html {
  height: 100%;
  font-family: 'Pacifico', cursive;
  font-family: 'IBM Plex Sans', sans-serif;
  background: #E4DAD6;
}
.app-title {
  text-align: center;
  font-family: 'Pacifico';
  font-size: 5rem;
  font-weight: 3;
}
</style>
