<template>
    <div class="album-container">
        <div class="row" v-for="(elm,index) in filteredList" :key="index">
            <Cover :copertina="elm"/>
        </div>
    </div>
</template>

<script>
import Cover from './Cover.vue';
import axios from 'axios';

export default {
    name:"Albums",
    props:["infoGenre"],
    components:{
        Cover
    },
    data(){
        return{
            album:[]
        }
    },
    computed:{
        filteredList(){
            return this.album.filter((value)=>{
                return value.genre.toLowerCase().includes(this.infoGenre.toLowerCase());
            }
            )}
    },
    created() {
		axios.get("https://flynn.boolean.careers/exercises/api/array/music")
			.then( (res) => {
				this.album = res.data.response;
			});
	}
}
</script>

<style lang="scss" scope>
.album-container{
    display:flex;
    width: 70%;
    margin: 0 auto;
    flex-wrap: wrap;
    justify-content: center;
    padding-top:50px;

    .row{
        display: flex;
        justify-content: center;
        padding:20px 15px ;
        text-align: center;
    }
    
}
</style>