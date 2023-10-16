<template>

  <div class="container">
  <Header></Header>
    <MyApps></MyApps>
</div>
</template>

<script>
import Header from './components/Header'
import MyApps from './components/myApps.vue'
// import Wall from './img/wall.jpg'
  export default {
      name : 'App',
      components : {
          Header,
          MyApps,
      }
  }
</script>

<style> 



body {
  font-family: -apple-system, BlinkMacSystemFont, sans-serif;
  overflow: hidden;
  background-image: url('img/wall.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  height: 100vh;
  
  /* margin: 0; */
  min-width: 600px;
  min-height: 600px;
}

@media screen and (min-width: 640px) {
  body {
    background-image: url('img/iphone.jpg');
    background-color: green;
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

