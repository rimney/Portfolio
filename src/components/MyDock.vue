<template>
    <div class="Dock" v-if="showDock">
        <div class="dockIcons">
          <div class="dockIcon">
            <img src="../img/contact.png" alt="">
          </div>
          <div class="dockIcon">
            <img id="emailimg" src="../img/email.png" alt="">
          </div>
          <div class="dockIcon">
            <img id="calendarImg" src="../img/calendar.png" alt="">
          </div>
          <div class="dockIcon">
            <img src="../img/github.png" alt="">
          </div>
          <div class="dockIcon">
            <img src="../img/darkmode.png" alt="">
          </div>



        </div>
    </div>
  </template>
  
  <script>
    export default {
  data () {
    return {
      showDock : true
    }
  },
        name : 'MyDock',
        components : {
        }
        
    }
  </script>
  
  <style scoped> 
.Dock {
    border-radius: 14px;
    height: 69px;
    width: 390px;
    background-color: rgba(0, 0, 0, 0.58);
    position: fixed;
    bottom: 11px;
    left: 50%;
    transform: translateX(-50%);
}
#emailimg
{
  width : 58px;
  height: 58px;
}

#calendarImg
{
  margin-left: 7px;
  margin-top: 5px;
  width: 50px;
  height: 50px;
}
.dockIcons
{
  margin-top : 5px;
  display: flex;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;

}
.dockIcon img {
  cursor:pointer;

    padding-right: 6px;
    width: 60px;
    height: 60px;
    transition: transform 0.3s ease; /* Added transition property */
}

  .dockIconEmail img
  {
    width : 60px;
  }

  .dockIcon:hover img {
    transform: scale(1);
    /* margin: 1 1em; */
    transition: transform 0.3s ease; /* Added transition property */
}

.dockIcon:hover img {
    transform: scale(1.2);
    /* margin: 0 1em; */
    transition: transform 0.1s ease; /* Added transition property */
}
  </style>
  
  