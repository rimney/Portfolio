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
                <span id="about">Contact</span>
            </div>
            <div class="modalBody">
                <div class="imgName">
                    <div class="myimg">
                        <img src="../img/rimney.jpeg" alt="">
                        <h3 id="me">RIYAD MNEY</h3>
                    </div>
                </div>
                <div class="contactInfo">
                    <div class="contactTitle">
                        <span>Email</span>
                        <span>Discord</span>
                        <span>Number</span>
                        <span>LinkedIn</span>
                    </div>
                    <div class="contactData">
                        <span>Rimney13@gmail.com</span>
                        <span>Rimney</span>
                        <span>(+212)0680344281</span>
                        <span>Rimney13</span>

                    </div>
                </div>
                <div class="contactInfoPhone">
                    <div class="Datacontainer">
                        <span id="infoTitle">Mobile</span>
                        <span id="infoData">+212 6 80 34 42 81</span>
                    </div>
                    <div class="Datacontainer">
                        <span id="infoTitle">Mobile</span>
                        <span id="infoData">+212 6 80 34 42 81</span>
                    </div>
                    <div class="Datacontainer">
                        <span id="infoTitle">Mobile</span>
                        <span id="infoData">+212 6 80 34 42 81</span>
                    </div>
                    <div class="Datacontainer">
                        <span id="infoTitle">Mobile</span>
                        <span id="infoData">+212 6 80 34 42 81</span>
                    </div>


                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            windowWidth: window.innerWidth,
            windowHeight: window.innerHeight,
        }
    },
    methods: {
        close() {
            this.$emit("close");
        },
    },

};
</script>
  
<style scoped>
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

.contactInfoPhone {
    display: none;
}

.modal-inner {
    width: 300px;
    background-color: white;
    border-radius: 0.5em;
    padding: 1em;
    background-color: rgba(36, 36, 36, 36);
    border: white solid 0.5px;
}

.header {
    width: 300px;
    height: 12px;
    display: flex;
    margin-bottom: 30px;
    align-items: center;
}

.buttons {
    display: flex;
    padding-right: 70px;
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
    height: 400px;
}

.imgName {
    width: 100%;
    height: 200px;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.myimg {
    color: rgb(147, 147, 147);

    display: flex;
    border-radius: 100px;
    width: 150px;
    height: 160px;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;



}

.myimg img {
    border-radius: 100px;
    width: 150px;
    height: 150px;
}

.contactInfo {
    width: 100%;
    height: 200px;
    display: flex;
    justify-content: space-between;
}

.contactTitle {
    padding-top: 0.5px;
    font-size: 10px;
    width: 100px;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-end;

}

.contactData {
    color: rgb(147, 147, 147);
    font-size: 12px;
    width: 190px;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-start;
}

@media screen and (max-width: 640px) {

    @keyframes slide-in {
  from {
    transform: translateX(100%);
  }
  to {
    transform: translateX(0);
  }
}

@keyframes slide-out {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100);
  }
}
    .imgName {
        width: 100%;
        height: 200px;
        display: flex;
        align-items: center;
        flex-direction: column;
        margin-top: 8vh;
    }

    #me {
        color: white;
    }

    .contactInfo {
        display: none;
    }

    .contactInfoPhone {
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 100%;
        width: 100%
    }

    .closePhone img {
        /* margin-left: 6vw; */

        width: 38px;
        height: 40px;

    }

    .closePhone {
        margin-top: 20vh;
        margin-right: 6vw;
        display: block;
    }

    .Datacontainer {
        background-color: rgb(36, 36, 36);
        width: 90%;
        height: 10%;
        border-radius: 6px;
        min-width: 300px;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        margin-bottom: 3vh;
    }

    .Datacontainer span {
        margin-left: 14px;
        color: rgb(24, 89, 202);
    }

    #infoTitle {
        color: white;
    }

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
        /* height: 100vh; */
        /* Full height of viewport */
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: rgba(0, 0, 0, 0.5);
        /* Semi-transparent black background */
        z-index: 9999;
        animation: slide-in 0.3s ease-in-out;

        /* Ensure it's above all other elements */
    }
    .modal-enter-active {
  /* Add animation property for sliding effect */
  animation: slide-in 0.3s ease-in-out;
}

.modal-leave-active {
  /* Add animation property for sliding effect */
  animation: slide-out 0.3s ease-in-out;
}

    .modalBody img {

        width: 70%;
        height: 70%;
        /* min-width: 413px; */
        /* min-height: 600px; */
        border-radius: 100px;
    }

    .modal-inner {
        width: 100vw;
        height: 100vh;
        transition: all 0.3s ease;
        background-color: black;
    }

    .modalBody {
        width: 100vw;
        height: 80vh;
    }
}</style>