<template>
    <header>
        <div>
            <img src="../assets/images/spotify-logo.png" alt="logo spotify">
        </div>

    </header>
</template>

<script>
export default {
    name:"Header"
}
</script>

<style lang="scss" scope>
@import '../assets/style/variables';
header{
    background-color: $secondaryColor;
    height:55px ;
    width:100%;

    img{
        height: 45px;
        margin: 5px 10px;
    }

}
</style>