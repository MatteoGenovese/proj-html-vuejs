<template>
    <header>
        <section class="contacts">
            <div class="container">
                <div class="open-hours">
                    Open Hours: Mon - Sat - 9:00 - 18:00
                </div>
                <div class="telephone">
                    +1 (305) 1234-5678
                </div>
                <div>
                    hello@example.com
                </div>
                <div class="social">
                    <div id="facebook-icon">
                        f
                    </div>
                    <div id="tweeter-icon">
                        t
                    </div>
                    <div id="linkedin-icon">
                        in
                    </div>
                </div>
            </div>
        </section>
    </header>
</template>

<script >
export default {
    name: 'Header',

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

header {
    
}

.contacts{
    background-color: $seventh_color;
    color: $fifth_color;
}
.contacts > *{

    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 50px;


    &>* {
        padding-right: 5px;
        padding-left: 5px;

        &>* {
            padding-right: 5px;
            padding-left: 5px;
        }
    }

    .open-hours {
        flex-grow: 1;
    }

    .social {
        display: flex;
    }
}
</style>