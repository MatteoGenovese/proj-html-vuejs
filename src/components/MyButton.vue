<template>

    <a v-if="buttonType == 'light-blue'" class="light-blue-button button d-flex align-items-center" :href="link" :class="classBtn">
        {{ msg }}
    </a>
    <a v-else-if="buttonType == 'bgc-none'" class="bgc-none-button button d-flex align-items-center" :href="link" :class="classBtn">
        {{ msg }}
    </a>
    <a v-else-if="buttonType == 'light-blue-colors'" class="light-blue-colors button d-flex align-items-center" :href="link" :class="classBtn">
        {{ msg }}
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

a.button {
    height: 3rem;
    text-decoration: none;
    border-radius: .5rem;
    padding: 0.8rem 1.8rem;
    font-size: $button_fs;
    font-weight: $button_fw;
    display: inline-block;
    &:hover{
        animation-name: btnUp;
        animation-duration: 0.5s;
        animation-fill-mode: forwards;
        box-shadow: 0 1rem 2rem rgba($color: $fourth_color, $alpha: 0.5);
        cursor: pointer;
    }
    &:active{
        box-shadow: 0 .5rem 1rem rgba($color: $fourth_color, $alpha: 0.5);
        cursor: pointer;
    }
}

a.light-blue-colors {
    color: $fourth_color;
    border: .1rem solid $fourth_color ;
    &:hover {
        background-color: $fourth_color;
        color: $second_color;
    }
}

a.light-blue-button,
a.bgc-none-button {
    &:hover {
        background-color: $second_color;
        color: $fourth_color;
    }
}

a.light-blue-button {
    background-color: $sixth_color;
    color: $second_color;
}

a.bgc-none-button {
    color: $second_color;
    border: .1rem solid $sixth_color ;
}

@keyframes btnUp{
    0%{
        transform: translateY(0);
    }
    100%{
        transform: translateY(-1rem);
    }
}
</style>