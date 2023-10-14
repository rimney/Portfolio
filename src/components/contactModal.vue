<template>
    <div class="modal">
        <div class="modal-inner">
            <div class="header">
                <div class="buttons">
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
                    <span id="me">riyad mney</span>
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
    width: 300px;
    /* height: 300px; */
    background-color: white;
    border-radius: 0.5em;
    padding: 1em;
    /* margin: auto; */
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
    width : 100%;
    height:  400px;
}

.imgName
{
    width: 100%;
    height: 300px;
    display: flex;
    align-items: center;
    flex-wrap: nowrap;
    flex-direction: column;
    background-color: red;
}

.myimg
{
    display: flex;
    border-radius: 100px;
    background-color: green;
    width: 150px;
    height: 150px;
    flex-direction: column;
    align-items: center;

}
.myimg img
{
    border-radius: 100px;
    width : 150px;
    height: 150px;
}











</style>