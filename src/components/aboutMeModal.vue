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
                <span id="about">About Me</span>
            </div>
            <div class="modalBody">
                <div class="image">
                    <img src="../img/rimney.jpeg" alt="">
                    <h3>RIYAD MNEY</h3>
                    <h4>Software Engineer</h4>
                </div>
            </div>
            <div class="description">
                <p>Software engineer with expertise in building cutting-edge web applications. My skills are allowing me to
                    create seamless and user-friendly experiences.</p>
                <span id="skills">Skills</span>
                <p>ReactJS | VueJS | HTML | CSS | TailWind | JavaScript | TypeScript | Docker | Git | C | C++ | Unix | SQL |
                    GraphQL | NestJS</p>
            </div>
            <div class="phoneContainer">
                <div class="pContainer">
                    <div class="subtitle">
                        <span>FRAMEWORKS</span>
                    </div>
                    <div class="title">
                            <span>List Of Technologies I Use</span>
                    </div>
                    <div class="images">

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
            isResumeModalVisible: true, // Add this property to manage dropdown visibility
        };
    },
    methods: {
        close() {
            this.$emit("close");
        },
    },
};
</script>
  
<style scoped>
.closePhone {
    display: none;
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

#about {
    color: rgb(162, 157, 157);

}

.modal-inner {
    width: 500px;
    height: 500px;
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

.phoneContainer {
    display: none;
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
    /* background-color: green; */
    width: 100%;
    height: 250px;
    display: flex;
    justify-content: space-around;
    align-content: space-between;
    flex-direction: row;
    align-items: flex-start;
}

.modalBody .image {
    width: 160px;
    height: 160px;
    border-radius: 100px;
    border: 3px solid rgb(87, 82, 82);
}

.modalBody .image img {
    width: 160px;
    height: 160px;
    border-radius: 100px;
}

.modalBody .image h3 {
    color: rgba(182, 172, 172, 0.889);
    text-align: center;
}

.modalBody .image h4 {
    text-align: center;
    color: white;
}



#skills {
    font-size: large;
    font-weight: 500;
}

.description {
    display: flex;
    flex-direction: column;
    align-content: center;
    align-items: center;
    
}

.description p {
    text-align: center;
    
}

@media screen and (max-width: 640px) {
    
    
    .subtitle
    {
        background-color: rgb(28, 27, 29);
        width : 100%;
        height: 10%;
        border-top-left-radius: 30px;
    border-top-right-radius: 30px;
    display: flex;
    align-items: center;
    color : rgb(150, 150, 156)
}

.title
{
    background-color: rgb(28, 27, 29);
    width : 100%;
    height: 12%;
}

.subtitle span
{
    padding-left: 12px;
    font-weight: 550;
}

.title span
{
    font-weight: 550;
    font-size: 26px;
    padding-left: 12px;
}

.images
{
    border-bottom-left-radius: 30px;
    border-bottom-right-radius: 30px;
    /* background-color: rgb(28, 27, 29); */
    background-color: red;
    width : 100%;
    height: 70%;
}

.phoneContainer
{
    overflow-y: scroll;
    display: block;
    background-color: black;
    height: 100vh;
    width : 100vw;
    display: flex;
    justify-content: center;
    /* align-items: center; */
}

.pContainer
{
    min-width: 400px;
    /* width: 80%; */
    border-radius: 30px;
    margin: 40px;
    /* min-width : 80vw; */
    height: 50vh;
}
    .description {
        display: none;
    }
    
    .closePhone img {
        margin-left: 5vw;
        
        width: 38px;
        height: 40px;
        
    }
    
    .closePhone {
        /* margin-top: 20vh; */
        margin-right: 6vw;
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
        /* left: -0.1vh; */
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
    
    .modal-inner {
        width: 100vw;
        height: 100vh;
        transition: all 0.3s ease;
        background-color: green;
        
    }
    
    .modalBody {
        display: none;
    }
}
</style>