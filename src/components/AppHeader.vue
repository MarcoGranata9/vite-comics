<script>
export default {
    data() {
        return {
            navItems: [
                {
                    title: "CHARACTERS",
                    isActive: false   
                },
                {
                    title: "COMICS",
                    isActive: true   
                },
                {
                    title: "MOVIES",
                    isActive: false   
                },
                {
                    title: "TV",
                    isActive: false   
                },
                {
                    title: "GAMES",
                    isActive: false   
                },
                {
                    title: "COLLECTIBLES",
                    isActive: false   
                },
                {
                    title: "CHARACTERS",
                    isActive: false   
                },
                {
                    title: "VIDEOS",
                    isActive: false   
                },
                {
                    title: "FANS",
                    isActive: false   
                },
                {
                    title: "SHOP",
                    isActive: false   
                },
            ]
        }
    }
}
</script>

<template>
    
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="Dc logo">
            </div>
            <nav>
                <ul>
                    <li v-for="item in navItems" :key="item.title"><a href="">{{ item.title }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
    height: 120px;
    @include flex(center, center, row);
    .container {
        @include flex(space-between, center, row);

            ul {
                @include flex(center, center, row);
                gap: 1rem;
                list-style: none;
                
                a {
                    color: black;
                    text-decoration: none;
                    font-size: 0.9rem;
                    font-weight: bold;
                    padding-bottom: 47px;
                    &:hover {
                        border-bottom: 5px solid $primary;
                        color: $primary;
                    }
                }
            }
        }
    }
</style>