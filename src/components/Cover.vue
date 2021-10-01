<template>
  <div>
      <div class="card">
          <img :src="copertina.poster" :alt="copertina.title">
          <h3>{{copertina.title}}</h3>
          <div>{{copertina.author}}</div>
          <div>{{copertina.year}}</div>
      </div>
  </div>
</template>

<script>
export default {
    name:"Cover",
    props:["copertina"]
}
</script>

<style lang="scss" scope>
@import '../assets/style/variables';
.card{
    background-color:$secondaryColor ;
    height: 250px;
    width:150px;
    
    img{
        height: 115px;
        width: 115px;
        margin-top:15px;
    }
    h3{
        color:white;
        text-transform: uppercase;
        font-size: 15px;
        padding:10px 15px;
    }
    div{
        color:grey;
        font-size:14px;
    }
}
</style>