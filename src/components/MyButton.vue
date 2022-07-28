<template>

    <a v-if="buttonType == 'light-blue'" class="light-blue-button button" :href="link" :class="classBtn">
        {{msg}}
    </a>
    <a v-else-if="buttonType=='bgc-none'" class="bgc-none-button button" :href="link" :class="classBtn">
        {{msg}}
    </a>
</template>

<script>
export default {
    name: 'MyButton',
    props: {
        buttonType: {
            type: String,
            required: true,
        },
        link: {
            type: String,
        },
        msg: {
            type: String,
        }
        ,
        classBtn: {
            type: String,
        }
    }

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

a.button{

    height: 50px;
    text-decoration: none;
    border-radius: 5px ;
    padding: 0.5rem 1.7rem;
    font-size: $button_fs;
    font-weight: $button_fw;
    

}
a.button.light-blue-button,
a.button.bgc-none-button{
    &:hover{
        background-color: $second_color;
        color: $fourth_color;
    }
}

a.button.light-blue-button{
        background-color: $sixth_color;
        color: $second_color;
        
}
a.button.bgc-none-button{
        color: $second_color;
        border: 1px solid $sixth_color ;
        

}
</style>