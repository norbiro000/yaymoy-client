<template>
  <div id="app" class="">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=IBM+Plex+Sans|Pacifico");
body,
html {
  height: 100%;
  font-family: "IBM Plex Sans", sans-serif;
  background: #fdfefe;
}
#app {
}

.button-close {
  height: 30px;
  width: 30px;
  border-radius: 30px;
  background: #333333c4;
  color: white;

  &:hover {
    background: #333333d3;
    transition: background 160ms;
  }
}

.shadow-1 {
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.15);
}

.shadow-2 {
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.15);
}
</style>
