<template>
    <div class="apps">
        <div class="icons">
            <div class="icon">
                <img src="../img/adobe.png" alt="">
                <span>Resume</span>
            </div>
            <div class="icon">
                <img src="../img/finder.png" alt="">
                <span>Projects</span>
            </div>
            <div class="icon">
                <img src="../img/contact.png" alt="">
                <span>Contact</span>
            </div>
            <div class="icon">
                <img src="../img/linkedin.png" alt="">
                <span>LinkedIn</span>
            </div>
            <div class="icon">
                <img src="../img/github.png" alt="">
                <span>GitHub</span>
            </div>

        </div>
    </div>
</template>
<script>
export default {
    name: 'MyApps',
}
</script>
<style scoped>
.apps {
    width: 50%;
    height: 800px;
    /* background-color: green; */
    margin-top: 2%;
}

.apps img {
    cursor:pointer;

    width: 65px;
    height: 65px;
    border-radius: 7px;

}
.icon span
{
    cursor:pointer;

}
.icons{

    display: flex;
    justify-content: center;
    align-content: flex-start;
    flex-direction: column;
    flex-wrap: wrap;
    margin-top: 40px;
}

.icon {
    cursor:pointer;

    height: 100px;
    font-size: 15px;
    color : white;
    display: flex;
    align-items: center;
    flex-direction: column;
    border-radius: 20px;
}




</style>