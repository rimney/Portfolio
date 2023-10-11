 <template>
    <button :style={background:color} class="btn">
        {{text}}
    </button>

 </template>

<script>
 export default {
    name : 'AppButton',
    props : {
        text : String,
        color : String,
    }
 }

</script>

<style scoped>
.btn{
    color : white;
    margin-right: 10px;
    width : 100px;
    height : 50px;
    background-color : black;
    border-radius: 10px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    font-size: 20px;
}
</style>