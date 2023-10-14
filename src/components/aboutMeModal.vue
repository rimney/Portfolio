<template>
    <div class="modal">
        <div class="modal-inner">
            <div class="header">
                <div class="buttons">
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
                <p>Software engineer with expertise in building cutting-edge web applications. My skills are allowing me to create seamless and user-friendly experiences.</p>
                <span id="skills">Skills</span>
                <p>ReactJS | VueJS | HTML | CSS | TailWind | JavaScript | TypeScript | Docker | Git | C | C++ | Unix | SQL | GraphQL | NestJS</p>
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
    border : 3px solid rgb(87, 82, 82);
}

.modalBody .image  img{
    width: 160px;
    height: 160px;
    border-radius: 100px;
}
.modalBody .image  h3 {
    color : rgba(182, 172, 172, 0.889);
    text-align: center;
}

.modalBody .image h4
{
    text-align: center;
    color : white;
}

.description{

    /* width: 522px; */
    /* height: 150px; */
    /* flex-direction: column; */
    /* justify-content: center; */
}

#skills
{
    font-size: large;
    font-weight: 500;
}

.description
{
    display: flex;
    flex-direction: column;
    align-content: center;
    align-items: center;

}
.description p
{
    text-align: center;

}


</style>