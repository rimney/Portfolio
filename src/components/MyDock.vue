<template>
    <div class="Dock" v-if="showDock">
        <div class="dockIcons">
          <div class="dockIcon">
            <img @click="openContactModalInternal" src="../img/contact.png" alt="">
          </div>
          <div class="dockIcon">
            <img id="emailimg" src="../img/email.png" @click="sendEmail"  alt="">
            
          </div>
          <div class="dockIcon">
            <img @click="openResumeModal" id="resume" src="../img/adobe.png" alt="">
          </div>
 
          <div class="dockIcon">
            <img @click="openAboutMeModalInternal" src="../img/finder.png" alt="">
          </div>

        </div>
    </div>
  </template>
  
  <script>
    export default {
  methods: {
    openContactModalInternal() {
            this.$emit('open-contact-modal'); // Emitting a custom event
        },
    openAboutMeModalInternal() {
            this.$emit('open-about-me-modal'); // Emitting a custom event
        },
    openResumeModal()
    {
      this.$emit('open-resume-modal');
    },
    sendEmail() {
      const email = "rimney13@gmail.com"; // Replace EMAILADDRESS with the recipient's email address
      window.location.href = `mailto:${email}`;
    }
  },
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
  border-radius: 7px;
  margin-left: 7px;
  margin-top: 2px;
  width: 55px;
  height: 55px;
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
  
  