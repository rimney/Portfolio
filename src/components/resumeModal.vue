<template>
    <div class="modal">
        <div class="modal-inner">
            <div class="header">
                <div class="buttons">
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
    height: 700px;
    background-color: white;
    border-radius: 0.5em;
    padding: 1em;
    /* margin: auto; */
    background-color: rgba(36, 36, 36, 36);
    border: white solid 0.5px;

}

.header {
    width: 500px;
    height: 12px;
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
    width : 100%;
    height:  650px;
}
.modalBody img {
    width : 100%;
    height:  660px;
    margin-bottom: 10px;
    border-radius: 10px;
}












</style>