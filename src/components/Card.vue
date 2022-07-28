<template>
<div class="card d-flex flex-column" v-if="!card.isFeedback">
    <div class="card-img-container d-flex justify-content-between">
        <img src="../assets/truck-1.png" alt="">
        <div>freccia</div>
    </div>
    <div class="card-title">
       {{card.cardTitle}}
    </div>
    <div class="card-description">
           {{card.cardDescription}}
    </div>
</div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        card:{
            type:Object,
            required:true,
        },
    }

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

div.card{
    width: calc( ( 100% / 3 ) - 20px );
    background-color: rgba($third_color,0.1);
    padding: 4rem 3rem;
}
div.card-img-container{
    height: 60px;
    img{
        height: 100%;
    }
}
div.card-title{
    font-size: 1.8rem;
    font-weight: 800;
}


</style>