<template>
    <div class="modal">
        <div class="modal-inner">
            <div class="header">
                <div class="buttons">
                    <div @click="close" class="exitPhone" v-show="windowWidth <= 600">
                        <span>X</span>
                    </div>
                    <div class="closeX" @click="close"><span>x</span></div>
                    <div class="closeY" @click="close"></div>
                    <div class="closeY" @click="close"></div>
                </div>
                <span id="about">Projects</span>
            </div>
            <div class="modalBody">
                <div class="projects">
                    <div class="project" v-for="project in array" :key="project.projectName">
                        <div class="projectContainer">
                            <div class="projectData">
                                <div class="projectTitle">
                                    <h2>{{ project.projectName }}</h2>
                                </div>
                                <div class="projectDescription">
                                    <p>{{ project.projectDescription }}</p>
                                    <a :href="project.projectLink">Read More...</a>
                                </div>
                            </div>
                            <div class="projectImage">
                                <img :src="project.imagePath" alt="" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import images from '../img/images.js';
export default {
    data() {
        return {
            windowWidth: window.innerWidth,
            windowHeight: window.innerHeight,
            array: [
                {
                    projectName: "Inception",
                    projectDescription: "Inception is a project that focuses on containerization using Docker. The main objective of this project is to create a LEMP stack that has WordPress on it hosted by NGINX and PHP FPM. It also has a MariaDB that communicates with it using Docker network.",
                    projectLink: "https://github.com/rimney",
                    imagePath: images.inception
                },
                {
                    projectName: "Ft_transendance",
                    projectDescription: "Inception is a project that focuses on containerization using Docker. The main objective of this project is to create a LEMP stack that has WordPress on it hosted by NGINX and PHP FPM. It also has a MariaDB that communicates with it using Docker network.",
                    projectLink: "https://github.com/rimney",
                    imagePath: images.webserv
                },
                {
                    projectName: "Webserv",
                    projectDescription: "Inception is a project that focuses on containerization using Docker. The main objective of this project is to create a LEMP stack that has WordPress on it hosted by NGINX and PHP FPM. It also has a MariaDB that communicates with it using Docker network.",
                    projectLink: "https://github.com/rimney",
                    imagePath: images.webserv
                },
                {
                    projectName: "Rimney.me",
                    projectDescription: "Inception is a project that focuses on containerization using Docker. The main objective of this project is to create a LEMP stack that has WordPress on it hosted by NGINX and PHP FPM. It also has a MariaDB that communicates with it using Docker network.",
                    projectLink: "https://github.com/rimney",
                    imagePath: images.minishell
                }
            ]
        };
    },
    methods: {
        close() {
            console.log(this.array[1].projectName);
            this.$emit("close");
        },
    },
};
</script>
  
<style scoped>
.Dock {
    display: none;
}

.modalBody::-webkit-scrollbar {
    width: 10px;
    /* Set the width of the scrollbar */
}

.modalBody::-webkit-scrollbar-thumb {
    background-color: #888;
    /* Set the color of the scrollbar thumb */
    border-radius: 5px;
    /* Optional: round the corners of the thumb */
}

.exitPhone {
    display: none;
}

.modalBody::-webkit-scrollbar-track {
    background-color: #1e1b1b;
    /* Set the color of the scrollbar track */
}

.modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;

    justify-content: center;
}

.modal-inner {
    width: 80vw;
    height: 84vh;
    background-color: white;
    border-radius: 0.5em;
    padding: 1em;
    margin: auto;
    background-color: black;
    border: white solid 0.5px;
}

.header {
    width: 500px;
    height: 20px;
    display: flex;
    margin-bottom: 30px;
    align-items: center;
}

.buttons {
    display: flex;
    padding-right: 160px;
}

.closeX {
    cursor: pointer;
    margin-right: 5px;
    font-size: 12px;
    color: white;
    width: 12px;
    height: 12px;
    background-color: rgb(240, 97, 80);
    display: flex;
    border-radius: 100px;
    justify-content: space-around;
    align-content: space-between;
    align-items: flex-end;
}

.closeY {
    cursor: pointer;

    margin-right: 5px;
    font-size: 12px;
    color: white;
    width: 12px;
    height: 12px;
    background-color: rgb(82, 82, 82);
    display: flex;
    border-radius: 100px;
    justify-content: space-around;
    align-content: space-between;
    align-items: flex-end;
}

.modalBody {
    width: 100%;
    height: 94%;
    overflow: scroll;
}

.project {
    margin-top: 20px;
    background-color: rgb(50, 50, 50);
    width: 100%;
    height: 210px;
    border-radius: 14px;
    margin-bottom: 20px;
    transition: transform .2s;
    /* Animation */

}


.projectContainer {
    /* background-color: red; */

    display: flex;
    width: 100%;
    height: 100%;
}

.projectData {
    display: flex;
    width: 50%;
    height: 100%;
    flex-direction: column;
}

.projectTitle {
    width: 100%;
    height: 25%;
    display: flex;
    margin-left: 7px;
    /* align-items: center; */
    /* justify-content: center; */
    /* background-color: red; */
}

.projectDescription {
    padding-left: 7px;
    /* text-align: center; */
    display: flex;
    width: 100%;
    height: 80%;
    /* background-color: blue; */
    font-size: 14px;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-start;

}

.projectDescription p {
    margin-top: 5px;
    margin-bottom: 10px;
}

.projectDescription a {
    text-decoration: none;
    color: white;
}

.projectImage {
    /* background-color: green; */
    width: 50%;
    height: 100%;
    align-items: center;
    justify-content: center;
    display: flex;
}

.projectImage img {
    border-radius: 100px;
    width: 190px;
    height: 190px;
}

@media screen and (max-width: 640px) {
    .exitPhone {
        margin-left: 6vw;
        display: block;
    }

    header {
        display: none;
    }

    #about {
        display: none;
    }

    .closeY {
        display: none;
    }

    .closeX {
        display: none;
    }

    .header {
        font-size: 20px;
        width: 41vw;
        height: 38px;
        /* background-color: green; */
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: unset;
        color: rgb(29, 131, 246);
    }

    .modal {
        position: fixed;
        top: -2vh;
        left: 0;
        width: 100vw;
        /* Full width of viewport */
        height: 100vh;
        /* Full height of viewport */
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: rgba(0, 0, 0, 0.5);
        /* Semi-transparent black background */
        z-index: 9999;
        /* Ensure it's above all other elements */
    }

    .modal-inner {
        width: 100vw;
        height: 100vh;
        transition: all 0.3s ease;
    }

    .projects {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .project {
        /* aspect-ratio: 3/4; */
        margin-top: 20px;
        background-color: rgb(50, 50, 50);
        width: 90vw;
        height: 65vh;
        border-radius: 14px;
        margin-bottom: 20px;
        border-top-right-radius: 50px;
        border-top-left-radius: 50px;
    }

    .projectContainer {

        display: flex;
        width: 100%;
        height: 100%;
        justify-content: center;
        flex-direction: column-reverse;
    }


    .projectData {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        flex-direction: column;
    }

    .projectTitle {
        width: 100%;
        height: 25%;
        display: flex;
        margin-left: 7px;
        justify-content: center;
        /* align-items: center; */
        /* justify-content: center; */
        /* background-color: red; */
    }

    .projectDescription {
        padding-left: 7px;
        justify-content: space-between;
        margin-bottom: 2vh;
        align-items: center;
        text-align: center;
        display: flex;
        width: 100%;
        height: 100%;
        /* background-color: blue; */
        font-size: 14px;
        flex-direction: column;

    }

    .projectDescription p {
        margin-top: 5px;
        margin-bottom: 10px;
    }

    .projectDescription a {
        display: flex;
        background-color: rgb(29, 131, 246);
        width: 100px;
        height: 30px;
        text-align: center;
        text-decoration: none;
        color: white;
        align-items: center;
        align-content: center;
        justify-content: center;
        border-radius: 14px;
    }

    .projectImage {
        /* background-color: green; */
        width: 100%;
        height: 100%;
        align-items: center;
        justify-content: center;
        display: flex;

    }

    .projectImage img {
        width: 100%;
        height: 40vh;
        border-top-right-radius: 50px;
        border-top-left-radius: 50px;


    }

    .modalBody {
        width: 100vw;
        height: 80vh;
    }



}
</style>