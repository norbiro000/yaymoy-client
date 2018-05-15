<template>
  <div id="app" class="text-center">
    <div class="overlay"></div>
    <h1 class="landing-title center-screen white light">YaymoY</h1>
    <h3 class="center-screen--sub white light font1 m-t-10">is has no idea website, and not sure what's it will be. but 100% Serverless Project.</h3>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=IBM+Plex+Sans|Pacifico');
body, html {
  height: 100%;
  font-family: 'Pacifico', cursive;
  font-family: 'IBM Plex Sans', sans-serif;
}
#app {
  position: absolute;
  left: 0;
  top: 0;

  /* Full width */
  width: 100%;

  /* Full height */
  height: 100%;

  /* Set backgroud image */
  background-image: url('./assets/thailand-1375488-1600x1200.jpg');

  /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.text-center {
  text-align: center;
}

#app .landing-title {
  font-family: 'Pacifico';
  font-size: 3rem;
}

.light {
  font-weight: 10;
}

.white {
  color: white;
}

.center-screen {
  position: relative;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -60%);
}
.font-1 {
  font-family: 'IBM Plex Sans';
}
.center-screen--sub {
  position: relative;
  top: 30%;
  left: 50%;
  transform: translate(-50%, -60%);
}
.overlay {
  position: fixed;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  background-image: url('./assets/monkeys-on-hainan-island-1517814-1280x960.jpg');
  background: rgba($color: #000000, $alpha: 0.3);
}

/* Utilitu */
.m-t-10 {
  margin-top: 25px;
}
</style>
