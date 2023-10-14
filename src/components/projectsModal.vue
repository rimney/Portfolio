<template>
    <div class="modal">
        <div class="modal-inner">
            <div class="header">
                <div class="buttons">
                    <div class="closeX" @click="close"><span>x</span></div>
                    <div class="closeY" @click="close"></div>
                    <div class="closeY" @click="close"></div>
                </div>
                <span id="about">Projects</span>
            </div>
            <div class="modalBody">
                <div class="projects">
                    <div class="project">
                        <div class="projectContainer">
                            <div class="projectData">
                                <div class="projectTitle">

                                </div>
                                <div class="projectDescription">

                                </div>
                            </div>
                            <div class="projectImage">
                                <!-- <img src="" alt=""> -->
                                <div class="img"></div>
                            </div>
                        </div>
                    </div>
                    <div class="project">
                    </div>
                    <div class="project">
                    </div>
                    <div class="project">
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
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
    height: 670px;
    background-color: white;
    border-radius: 0.5em;
    padding: 1em;
    margin: auto;
    background-color: rgba(36, 36, 36, 36);
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
    height: 600px;
    overflow: scroll;
}

.project {
    margin-top: 20px;
    background-color: rgb(50, 50, 50);
    width: 100%;
    height: 200px;
    border-radius: 14px;
    margin-bottom: 20px;
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
    height: 50%;
    background-color: red;
}

.projectDescription {
    width: 100%;
    height: 50%;
    background-color: blue;
}

.projectImage
{
    background-color: green;
    width : 50%;
    height: 100%;
    align-items: center;
    justify-content: center;
    display: flex;
}

.projectImage .img
{
    border-radius: 120px;
    width : 180px;
    height: 180px;
    background-color: black;
}
</style>