<script>
export default {
    data() {
        return {
            imgArray: [
                {
                    path: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS"
                },
                {
                    path: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE"
                }, 
                {
                    path: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION"
                }, 
                {
                    path: "buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR"
                },    
            ], 
        }
    },
    methods: {
        getImagePath(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }            
    }
}
</script>

<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="img in imgArray" :key="img.path">
                    <a href="">
                        <img :src="getImagePath(img.path)" alt="">
                        <p>{{ img.text }}</p>
                    </a>
                </li>
                <li>
                    <a href="">
                        <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                        <p>DC POWER VISA</p>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

    section {
        background-color: $primary;
        padding: 50px 0;
        .container {
            width: 70%;
            margin: 0 auto;
            ul {
                @include flex(space-between, center, row);
                list-style: none;
                gap: 20px;

                a {
                    @include flex(center, center, row);
                    gap: 15px;
                    text-decoration: none;
                    color: white;
                    font-size: 0.8rem;
                    img {
                        width: 50px;
                        height: 65px;
                    }
                }
            }
        }
    }
</style>