<template>
    <div class="box">
        <p>knvlwdenlweknfkwe</p>
    </div>
</template>

<script>
export default {
    name: 'TextBox'
}
</script>

<style lang="scss" scoped>
@import '../assets/variables';

.box{
    margin: 3%;
    background-color: rgb(224, 224, 220);
    height: 40%;
    width: 20%;
    padding: 5%;
    box-sizing: border-box;
    box-shadow: 0px 0px 10px 5px rgba($darkblue, 0.55); //lengt hor, length ver, blur, spread
    border-radius: 25px;
}

</style>
