<template>
  <div class="cocntainer">
  <Header></Header>
    <MyApps></MyApps>
    <MyDock></MyDock>
</div>
</template>

<script>
import Header from './components/Header'
import MyApps from './components/myApps.vue'
import MyDock from './components/MyDock.vue'
// import Wall from './img/wall.jpg'
  export default {
      name : 'App',
      components : {
          Header,
          MyApps,
          MyDock,
      }
  }
</script>

<style> 
body
{
  font-family: -apple-system, BlinkMacSystemFont, sans-serif;
  overflow:hidden;
  background-image: url('img/wall.jpg');
  background-size: 2010px 1080px;
  background-repeat: no-repeat;

}
#app
{

}
</style>

