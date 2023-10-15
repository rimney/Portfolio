<template>
    <div class="apps">
        <div class="icons">
            <div class="icon">
                <img @click="openResumeModal" src="../img/adobe.png" alt="">
                <resumeModal v-show="isResumeModalVisible" @close="closeResumeModal"></resumeModal>
                <span>Resume</span>
            </div>
            <div class="icon">
                <img  @click="openProjectsModal" src="../img/finder.png" alt="">
                <projectsModal v-show="isProjectsModalVisible" @close="closeProjectsModal"></projectsModal>
                <span>Projects</span>
            </div>
            <div class="icon">
                <img @click="openContactModal" src="../img/contact.png" alt="">
                <contactModal v-show="isContactModalVisible" @close="closeContactModal"></contactModal>
                
                <span>Contact</span>
            </div>
            <div class="icon">
                <img @click="goToLinkedin" src="../img/linkedin.png" alt="">
                <span>LinkedIn</span>
            </div>
            <div class="icon">
                <img @click="goToGithub" src="../img/github.png" alt="">
                <span>GitHub</span>
            </div>

        </div>
    </div>
</template>
<script>
import resumeModal from './resumeModal.vue';
import contactModal from './contactModal.vue';
import ProjectsModal from './projectsModal.vue';
export default {
    data() {
        return {
            isResumeModalVisible : false,
            isContactModalVisible : false,
            isProjectsModalVisible : false,
            
        }
    },
    components : {
    resumeModal,
    contactModal,
    ProjectsModal
},
    name: 'MyApps',
    methods : {
        openResumeModal() {
        this.isResumeModalVisible = true;
      },
      closeResumeModal() {
        this.isResumeModalVisible = false;
      },
        openProjectsModal() {
        this.isProjectsModalVisible = true;
      },
      closeProjectsModal() {
        this.isProjectsModalVisible = false;
      },
        openContactModal() {
        this.isContactModalVisible = true;
      },
      closeContactModal() {
        this.isContactModalVisible = false;
      },
      goToLinkedin()
      {
        window.open('https://www.google.com', '_blank');

      },
      goToGithub()
      {
        window.open('https://www.google.com', '_blank');

      },
    }
}
</script>
<style scoped>
.apps {
    width: 50%;
    height: 800px;
    /* background-color: green; */
    margin-top: 2%;
}

.apps img {
    cursor:pointer;

    width: 65px;
    height: 65px;
    border-radius: 7px;

}
.icon span
{
    cursor:pointer;

}
.icons{

    display: flex;
    justify-content: center;
    align-content: flex-start;
    flex-direction: column;
    flex-wrap: wrap;
    margin-top: 40px;
}

.icon {

    height: 100px;
    font-size: 15px;
    color : white;
    display: flex;
    align-items: center;
    flex-direction: column;
    border-radius: 20px;
}


@media screen and (max-width: 640px) {

.apps {
    width: 100%;
    height: 800px;
    /* background-color: green; */
    margin-top: 2%;
}

.icons{
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-content: flex-start;
    flex-direction: row;
    flex-wrap: wrap;
    margin-top: 40px;
}
}

</style>