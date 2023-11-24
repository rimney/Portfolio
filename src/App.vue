<template>
  <div>
    <div v-if="!isLoaded && isFirstVisit" class="loadingScreen">
      <div class="appleLogo">
        <img src="./img/applelogoWhite.png" alt="">
      </div>
      <div class="progress">
        <div class="progress__bar"></div>
      </div>
    </div>
    <div v-show="isLoaded || !isFirstVisit">
      <div class="container">
        <Header></Header>
        <MyApps></MyApps>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header'
import MyApps from './components/myApps.vue'

export default {
  name: 'App',
  components: {
    Header,
    MyApps,
  },
  data() {
    return {
      isLoaded: false,
      isFirstVisit: true,
    };
  },
  mounted() {
    const isFirstVisit = localStorage.getItem('isFirstVisit');
    if (isFirstVisit === null) {
      localStorage.setItem('isFirstVisit', 'false');
    } else {
      this.isFirstVisit = false;
    }

    setTimeout(() => {
      this.isLoaded = true; // Set isLoaded to true when content is loaded
    }, 5000); // Change to the duration of your content loading process (5 seconds in this case)
  },
};
</script>

<style>
.loadingScreen {
  display: flex;
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  background-color: black;
  justify-content: center;
  align-content: center;
  flex-direction: column;
  align-items: center;
}

.appleLogo img {
  width: 81px;
  margin-bottom: 39px;
  height: 99px;
}

.progress {
  width: 200px;
  border: 2px solid white;
  height: 3px;
  border-radius: 16px;
}

.progress .progress__bar {
  height: 100%;
  width: 0%;
  background-color: white;
  animation: fill-bar 5s infinite;
}

@keyframes fill-bar {
  from {
    width: 0%;
  }
  to {
    width: 100%;
  }
}

body {
  font-family: -apple-system, BlinkMacSystemFont, sans-serif;
  overflow: hidden;
  /* background-image: url('img/wall.jpg'); */
  background-image: url('img/wall.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  height: 100vh;
  min-width: 600px;
  min-height: 600px;
}

@media screen and (min-width: 640px) {
  body {
    background-image: url('img/wall.jpg');
    background-size: cover;
    background-position: center center;
  }
}

#app {
  /* Additional styles for your app container */
}

.container {
  /* Styles for your main container */
}
</style>
