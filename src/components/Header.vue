<template>
    <header>
        <section class="contacts">
            <div class="container">
                <div class="open-hours"><i class="fa-solid fa-clock"></i> {{ contacts.openHours }}</div>
                <div class="telephone"><i class="fa-solid fa-phone"></i> {{ contacts.telephoneNumber }}</div>
                <div><i class="fa-solid fa-envelope"></i> {{ contacts.email }}</div>
                <div class="social">
                    <div id="facebook-icon"><i class="fa-brands fa-facebook-f"></i></div>
                    <div id="tweeter-icon"><i class="fa-brands fa-twitter"></i></div>
                    <div id="linkedin-icon"><i class="fa-brands fa-linkedin-in"></i></div>
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

header{
    font-size: 1.1rem;
}

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