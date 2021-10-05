<template>
    <header>
        <img src="../assets/images/spotify-logo.png" alt="logo spotify">
        <select name="" id="" @change="$emit('change',option)" :v-model="option">
            <option value="">Seleziona Genere</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </header>
</template>

<script>
export default {
    name:"Header",
    data(){
        return{
            option:"",
        }
    }
}
</script>

<style lang="scss" scope>
@import '../assets/style/variables';
header{
    background-color: $secondaryColor;
    height:55px ;
    width:100%;
    display:flex;
    justify-content: space-between;
    align-content: center;

    img{
        height: 45px;
        margin: 5px 10px;
    }
    select{
        margin:12px 15px;
        border-radius: 5px;
    }
    select:focus{
        outline: none;
    }

}
</style>