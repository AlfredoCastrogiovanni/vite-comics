<template>
    <header>
        <div class="wrapper">
            <div class="imgWrapper">
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>
            <nav>
                <ul>
                    <li v-for="link in navLinks" :class=" (link.active) ? 'active' : '' ">
                        <a :href="link.href">
                            {{ link.name }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {
        name: "AppHeader",
        data() {
            return {
                navLinks: [
                    {
                        name: "Characters",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Comics",
                        href: "#",
                        active: true
                    },
                    {
                        name: "Movies",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Tv",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Games",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Tv",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Collectibles",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Videos",
                        href: "#",
                        active: false
                    },
                    {
                        name: "News",
                        href: "#",
                        active: false
                    },
                    {
                        name: "Shop",
                        href: "#",
                        active: false
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @use "../styles/partials/variables" as *;
    @use "../styles/partials/mixins" as *;

    header {
        width: 100%;
        height: 110px;
        // @include flex();

        div.wrapper {
            width: $wrapper-width;
            margin: 0 auto;
            @include flex(row, space-between);
            div.imgWrapper {
                @include flex(row, center, center);

                img {
                    height: 65%;
                }
            }

            nav ul {
                height: calc(100% - 5px);
                @include flex(row, center);
                list-style: none;

                li {
                    line-height: 110px;
                    margin-right: 2rem;
                    text-transform: uppercase;
                    font-weight: bold;
                    font-size: 0.9rem;

                    &.active {
                        border-bottom: 5px solid $main-color;

                        a {
                            color: $main-color;
                        }
                    }
                }
            }
        }
    }
</style>