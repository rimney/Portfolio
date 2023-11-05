<template>
    <div class="apps">
        <div class="icons">
            <div class="icon">
                <img @click="openResumeModal" src="../img/adobe.png" alt="">
                <resumeModal v-show="isResumeModalVisible" @close="closeResumeModal"></resumeModal>
                <span>Resume</span>
            </div>
            <div class="icon">
                <img @click="goToLinkedin" src="../img/linkedin.png" alt="">
                <span>LinkedIn</span>
            </div>
            <div class="icon">
                <img @open-contact-modal="openContactModal" @click="openContactModal" src="../img/contact.png" alt="">
                <contactModal v-show="isContactModalVisible" @close="closeContactModal"></contactModal>

                <span>Contact</span>
            </div>
            <div class="icon">
                <img @open-about-me-modal="openAboutMeModal" @click="openAboutMeModal" src="../img/finder.png" alt="">
                <AboutMeModal v-show="isAboutMeModalVisible" @close="closeAboutMeModal"></AboutMeModal>

                <span>About Me</span>
            </div>
            <div class="icon">
                <img  @click="openProjectsModal" src="../img/projects.png" alt="">
                <projectsModal v-show="isProjectsModalVisible" @close="closeProjectsModal"></projectsModal>
                <span>Projects</span>
            </div>
            <div class="icon">
                <img @click="goToGithub" src="../img/github.png" alt="">
                <span>GitHub</span>
            </div>

        </div>

    </div>
    <MyDock v-show="showDock" @open-about-me-modal="openAboutMeModal"></MyDock>
</template>
<script>
import resumeModal from './resumeModal.vue';
import contactModal from './contactModal.vue';
import ProjectsModal from './projectsModal.vue';
import MyDock from './MyDock.vue'
import AboutMeModal from './aboutMeModal.vue';

export default {
    data() {
        return {
            windowWidth: window.innerWidth,
            windowHeight: window.innerHeight,
            isResumeModalVisible: false,
            isContactModalVisible: false,
            isProjectsModalVisible: false,
            showDock : true,
            isAboutMeModalVisible: false,
        }
    },
    components: {
    MyDock,
    resumeModal,
    contactModal,
    ProjectsModal,
    AboutMeModal
},
    name: 'MyApps',
    methods: {
        openResumeModal() {            
            if(this.windowWidth <= 600)
                this.showDock = false;
            this.isResumeModalVisible = true;
        },
        closeResumeModal() {
            this.showDock = true;
            this.isResumeModalVisible = false;
        },
        openProjectsModal() {
            if(this.windowWidth <= 600)
                this.showDock = false;
            this.isProjectsModalVisible = true;
        },
        closeProjectsModal() {
            this.showDock = true;
            this.isProjectsModalVisible = false;
        },
        openContactModal() {
            if(this.windowWidth <= 600)
            this.showDock = false;
        this.isContactModalVisible = true;
    },
    closeContactModal() {
        this.showDock = true;
            this.isContactModalVisible = false;
        },
        goToLinkedin() {
            window.open('https://www.google.com', '_blank');
            
        },
        goToGithub() {
            window.open('https://www.google.com', '_blank');
            
        },
        openAboutMeModal()
        {
            if(this.windowWidth <= 600)
                this.showDock = false;
            this.isAboutMeModalVisible = true;
        },

        closeAboutMeModal()
        {
            this.showDock = true;
            this.isAboutMeModalVisible = false;
        }
        ,
    }
}
</script>
<style scoped>
.apps {
    width: 50%;
    height: 800px;
    /* background-color: green; */
    margin-top: 2%;
    /* overflow: hidden; */
}

.apps img {
    cursor: pointer;

    width: 65px;
    height: 65px;
    border-radius: 7px;

}

.icon span {
    cursor: pointer;

}

.icons {

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
    color: white;
    display: flex;
    align-items: center;
    flex-direction: column;
    border-radius: 20px;
}


@media screen and (max-width: 640px) {

    .apps {
        width: 100%;
        height: 100%;
        /* background-color: green; */
        margin-top: 2%;
        position: fixed;
        top: 0%;
        left: 50%;
        transform: translateX(-50%);
    }

    .icons {
        /* width: 100%; */
        display: flex;
        justify-content: space-around;
        align-content: flex-start;
        flex-direction: row;
        flex-wrap: wrap;
        margin-top: 40px;
    }
}
</style>