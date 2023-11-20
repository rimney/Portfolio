<template>
    
    <div class="modal">
        <div class="modal-inner">
                <div class="header">
                    <div class="buttons">
                        <div @click="close" class="closePhone">
                        <img src="../img/exitPhoneWhite.png" alt="">
                    </div>
                    <div class="closeX" @click="close"><span>x</span></div>
                    <div class="closeY" @click="close"></div>
                    <div class="closeY" @click="close"></div>
                </div>
                <span id="about">Projects</span>
                <span> </span>
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
                                    <a id="readMore" :href="project.projectLink">Read More...</a>
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
                    projectName: "Rimney.me",
                    projectDescription: "Explore Rimney.me, your gateway to my digital world. Designed as a macOS session, represented in a sleek Mac-inspired interface. Crafted with Vue.js for dynamic interactivity and infused with classic CSS charm, Rimney.me offers a journey through my skills, projects, and personality. Dive in and discover the essence of my work in a uniquely nostalgic digital experience.",
                    projectLink: "https://github.com/rimney/Portfolio",
                    imagePath: images.minishell
                },
                {
                    projectName: "Inception",
                    projectDescription: "Inception is a project that focuses on containerization using Docker. The main objective of this project is to create a LEMP stack that has WordPress on it hosted by NGINX and PHP FPM. It also has a MariaDB that communicates with it using Docker network.",
                    projectLink: "https://github.com/rimney/inception",
                    imagePath: images.inception
                },
                {
                    projectName: "Ft_transendance",
                    projectDescription: "ft_transendance, your ultimate ping pong gaming hub! This single-page platform offers seamless login, enabling players to connect with friends, engage in one-on-one or group chats, and even watch live streams of fellow gamers in action. Immerse yourself in the thrill of ping pong, connect with a vibrant community, and elevate your gaming experience to new heights, all in one place!",
                    projectLink: "https://github.com/baraegh/ft_transcendence",
                    imagePath: images.trandandan
                },
                {
                    projectName: "Webserv",
                    projectDescription: "WebServ, a cutting-edge project crafted in C++, emulates the prowess of Nginx. Acting as a robust server, it efficiently handles HTTP requests by dynamically serving files within the project. Utilizing sockets and advanced data parsing techniques, WebServ ensures seamless communication, enabling users to experience rapid and reliable web hosting. Elevate your server-side capabilities with WebServ, the epitome of high-performance web handling.",
                    projectLink: "https://github.com/rimney/webserv",
                    imagePath: images.webserv
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

.closePhone {
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

#readMore
{
    margin-left: 3px;
    border-radius: 12px;
    display: flex;
    text-align: center;
    align-items: center;
    width : 100px;
    height: 25px;
    background-color: rgb(29, 131, 246);
    justify-content: center;
}

.modal-inner {
    max-width: 60vw;
    height: 75vh;
    border-radius: 0.5em;
    padding: 1em;
    margin: auto;
    background-color: rgb(30, 30, 30);
    border: white solid 0.5px;
}

.header {
    width: 94%;
    height: 20px;
    display: flex;
    margin-bottom: 30px;
    align-items: center;
    justify-content: space-between;
}

.buttons {
    display: flex;
}

.closeX {
    cursor: pointer;
    margin-right: 5px;
    font-size: 12px;
    color: rgb(141,23,16);
    width: 12px;
    height: 12px;
    background-color: rgb(240, 97, 80);
    display: flex;
    border-radius: 100px;
    justify-content: space-around;
    align-content: space-between;
    align-items: flex-end;
}

.closeX span{
    display: none;
}

.closeX:hover span{
    display: block;
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
    width: 58vw;
    height: 27vh;
    border-radius: 14px;
    margin-bottom: 20px;
    transition: transform .2s;
    padding-bottom: 10px;

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
}

.projectDescription {
    padding-left: 7px;
    display: flex;
    width: 100%;
    height: 80%;
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
    object-fit:cover;

}

@media screen and (max-width: 640px) {
    .closePhone {
        margin-right: 30vw;
    margin-top: 6vw;
    display: block;
    }
    .closePhone img 
    {
        width : 38px;
        height: 40px;
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
        max-width: 100vh;
        width: 100vw !important;
        height: 1400px;
        background-color: black;
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
        height: 55vh;
        border-radius: 14px;
        margin-top: 20vh;
        /* margin-bottom: 10vh; */
        border-top-right-radius: 10px;
        border-top-left-radius: 10px;
    }

    .projectContainer {

        display: flex;
        width: 100%;
        height: 70%;
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
        margin-bottom: 1vh;
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
        width: 90vw;
        height: 40vh;
        
        border-top-right-radius: 10px;
        border-top-left-radius: 10px;
        border-bottom-left-radius: 0px;
        border-bottom-right-radius: 0px;
    object-fit:cover;


    }

    .modalBody {
        width: 100vw;
        min-width: 80vw;
        height: 80vh;
        
        }



}
</style>