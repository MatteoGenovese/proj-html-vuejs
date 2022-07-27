<template>
    <div class="container">
        <h2>{{ page.extend_title }}</h2>
        <div v-if="page.highlitedPosition == 'before'">
            <h3 class="highlited-subtitle">{{ page.highlitedSubtitle }}</h3>
            <h3> {{ page.subtitle }}</h3>
        </div>
        <div v-else-if="page.highlitedPosition == 'none'">
            <h3>{{ page.subtitle }}</h3>
        </div>
        <div v-else>
            <h3>{{ page.subtitle }}</h3>
            <h3 class="highlited-subtitle"> {{ page.highlitedSubtitle }}</h3>
        </div>
        <p>{{ page.description }}</p>
    </div>
</template>

<script>
export default {
    name: 'SectionHeading',
    props: {
        page: {
            type: Object,
            required: true,
        },
    },

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.container h2 {
    color: $sixth_color;
    font-size: 1rem;
}

.container h3 {
    font-weight: 900;
    font-size: 2.5rem;
    display: inline-block;
            padding-left: 0.5rem;
        padding-right: 0.5rem;
}
.container .highlited-subtitle{
    
        background-color: $sixth_color;
        border-radius: 3px;


    

}

.container p {
    color: $third_color;
}
</style>