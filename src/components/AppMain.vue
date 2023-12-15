<template>
    <main>
        <div class="hero"></div>
        <ListComics/>
    </main>
</template>

<script>
    import ListComics from './ListComics.vue'

    export default {
        components: {
            ListComics
        }
    }
</script>

<style lang="scss" scoped>
    @use "../styles/partials/variables" as *;
    @use "../styles/partials/mixins" as *;

    main {
        background-color: $list-comics-color;
        .hero {
            width: 100%;
            height: 550px;
    
            background-image: url("../assets/img/jumbotron.jpg");
            background-repeat: no-repeat;
            background-size: cover;
            @include background(cover, start, no-repeat);
        }
    }
</style>