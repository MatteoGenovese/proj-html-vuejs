<template>
    <header>
        <section class="contacts">
            <div class="container">
                <div class="open-hours">{{ contacts.openHours }}</div>
                <div class="telephone"> {{ contacts.telephoneNumber }}</div>
                <div>{{ contacts.email }}</div>
                <div class="social">
                    <div id="facebook-icon">f</div>
                    <div id="tweeter-icon">t</div>
                    <div id="linkedin-icon">in</div>
                </div>
            </div>
        </section>

    </header>
</template>

<script >




export default {
    name: 'Header',
    props: {
        pages: {
            type: Array,
            required: true,
        },
        contacts: {
            type: Object,
            required: true,
        },
    },

    // add things here

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

section.contacts {
    background-color: $seventh_color;
    color: $second_color;
    height: 50px;
}

.contacts>*{
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    &>* {
        height: 100%;
        display: flex;
        align-items: center;
        padding-right: 5px;
        padding-left: 5px;
        ul{
            margin-bottom: 0;
        }
        &>* {
            height: 100%;
            display: flex;
            align-items: center;
            padding-right: 5px;
            padding-left: 5px;
            &>* {
                height: 100%;
                display: flex;
                align-items: center;
                padding-right: 5px;
                padding-left: 5px;
            }
        }
    }
}
.open-hours{
    flex-grow: 1;
}
.social {
    display: flex;
}
</style>