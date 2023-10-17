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
                <span id="about">Resume</span>
            </div>
            <div class="modalBody">
                <img src="../img/resume.png" alt="">
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

.modal-inner {
    width: 500px;
    height: 750px;
    background-color: white;
    border-radius: 0.5em;
    padding: 2em;
    margin: auto;
    background-color: rgba(36, 36, 36, 36);
    border: white solid 0.5px;
}
.closePhone
{
    display: none;
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
    height: 650px;
    display: flex;
    justify-content: center;
    /* background-color: green; */
}

.modalBody img {
    width: 100%;
    height: 660px;
    margin-bottom: 10px;
    border-radius: 10px;
}

@media screen and (max-width: 640px) {

    .closePhone img {
        margin-left: 6vw;

        width: 38px;
        height: 40px;

    }

    .closePhone { 
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
        /* Ensure it's above all other elements */
    }
    .modalBody img {
        width: 75%;
        height: 80%;
        min-width: 413px;
        min-height: 600px;
        border-radius: 2px;
    }
    .modal-inner {
        width: 100vw;
        height: 100vh;
        transition: all 0.3s ease;
        
    }
    .modalBody {
        width: 100vw;
        height: 80vh;
    }


}
</style>