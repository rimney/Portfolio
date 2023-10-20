
<template>
    <header>
        <div class="osHeader">
            <div class="leftSide">
                <img @click="toggleDropDown" src="../img/applelogoWhite.png" alt="">
                <div v-if="isDropDownVisible" class="dropdownMenu">
                    <span @click="openModal">About Me</span>
                    <span>Contact</span>
                    <span>My Projects</span>
                </div>
                <span>Finder</span>
                <span @click="openModal">About Me</span>
                <AboutMeModal v-show="isModalVisible" @close="closeModal"></AboutMeModal>
                <span>Projects</span>
                <span>Contact</span>
            </div>
            <div class="rightSide">
                <img src="../img/wifi.png" alt="">
                <img src="../img/siriIcon.png" alt="">
                <span>{{ currentDateTime }}</span> <!-- Display current date and time here -->
            </div>
        </div>
    </header>
</template>

<script>
import AboutMeModal from "./aboutMeModal.vue"; // Adjust the import path based on your project structure

export default {
  watch: {
  },
    name: 'AppHeader',
    components : {
        AboutMeModal,
    },
    data() {
        return {
            isDropDownVisible : false,
            currentDateTime: '',
            isModalVisible: false, // Add this property to manage dropdown visibility
        };
    },
    mounted() {
        // Update currentDateTime every second (1000 milliseconds)
        setInterval(() => {
            const daysOfWeek = ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'];
            const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'];

            const now = new Date();
            // Get day of the week, day, month, hours, and minutes in the desired format
            const formattedDateTime = `${daysOfWeek[now.getDay()]} ${this.formatTwoDigits(now.getDate())} ${months[now.getMonth()]} ${this.formatTwoDigits(now.getHours())}:${this.formatTwoDigits(now.getMinutes())}`;
            this.currentDateTime = formattedDateTime;
        }, 1000);
    },
    methods: {
        formatTwoDigits(num) {
            return num < 10 ? `0${num}` : num;
        },
        toggleDropDown() {
            this.isDropDownVisible = !this.isDropDownVisible; // Toggle dropdown visibility
        },
        openModal() {
            this.isDropDownVisible = false;
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      },
    }
}
</script>


<style scoped>


header {
    position: fixed;
    /* Set the position to fixed */
    top: 0;
    /* Stick the header to the top */
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 30px;
    background-color: rgba(0, 0, 0, 0.58);
    /* Optionally, add a background color */
    z-index: 1000;
    /* rgba(255, 255, 255, 0.183)igher z-index to ensure it's above other elements */
}

.osHeader {
    width: 100%;
    display: flex;
    justify-content: space-between;


}

.leftSide {
    color: white;
    display: flex;
    margin-left: 20px;
    width: 350px;
    align-content: space-between;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
}

.rightSide {
    color: white;
    display: flex;
    margin-right: 20px;
    width: 200px;
    align-content: space-between;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
}

.leftSide img {
    width: 16px;
    height: 18px;
}
</style>

<style scoped>
header {
    position: fixed;
    /* Set the position to fixed */
    top: 0;
    /* Stick the header to the top */
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 30px;
    background-color: rgba(0, 0, 0, 0.58);
    /* Optionally, add a background color */
    z-index: 1000;
    /* rgba(255, 255, 255, 0.183)igher z-index to ensure it's above other elements */
}

.osHeader {
    width: 100%;
    display: flex;
    justify-content: space-between;


}

.leftSide {
    color: white;
    display: flex;
    margin-left: 20px;
    width: 350px;
    align-content: space-between;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
}

.rightSide {
    color: white;
    display: flex;
    margin-right: 20px;
    width: 260px;
    align-content: space-between;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
}

.rightSide img 
{
    width : 20px;
    height : 20px;
}

.leftSide img {
    width: 16px;
    height: 18px;
}

.dropdownMenu {
    font-size : 13px;
    position: absolute;
    top: 100%;
    left: 0;
    background-color: rgba(0, 0, 0, 0.58);
    display: flex;
    width: 120px;
    height: 70px;
    border: 1px solid #ccc;
    box-shadow: 1px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 1000;
    flex-direction: column;
    border-radius: 4px;
    align-content: space-between;
    flex-wrap: nowrap;
    justify-content: space-around;
}
.dropdownMenu span:hover
{
    background-color: rgba(53, 21, 238);
}

@media screen and (max-width: 640px) {
  header {
    display: none;
  }
  .osHeader
  {
    display: none;
  }
}
</style>