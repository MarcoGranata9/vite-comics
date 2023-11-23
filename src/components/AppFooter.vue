<script>
export default {
    data() {
        return {
            comicsItems: [
                {
                    title: "Characters",
                },
                {
                    title: "Comics",
                },
                {
                    title: "Movies",
                },
                {
                    title: "TV",
                },
                {
                    title: "Games",
                },
                {
                    title: "Videos",
                },
                {
                    title: "News",
                },
            ],
            shopItems: [
                {
                    title: "Shop DC",
                },
                {
                    title: "Shop DC Collectibles",
                },
            ],
            DcItems: [
                {
                    title: "Terms Of Use",
                },
                {
                    title: "Privacy policy (New)",
                },
                {
                    title: "Ad Choices",
                },
                {
                    title: "Advertising",
                },
                {
                    title: "Jobs",
                },
                {
                    title: "Subscriptions",
                },
                {
                    title: "Talent Workshops",
                },
                {
                    title: "CPSC Certificates",
                },
                {
                    title: "Ratings",
                },
                {
                    title: "Shop Help",
                },
                {
                    title: "Contact Us",
                },
            ],
            sitesItems: [
                {
                    title: "DC",
                },
                {
                    title: "MAD Magazine",
                },
                {
                    title: "DC Kids",
                },
                {
                    title: "DC Universe",
                },
                {
                    title: "DC Power Visa",
                },
            ],
            imgFooter: [
                {
                    path: "footer-facebook.png"
                },
                {
                    path: "footer-twitter.png"
                },
                {
                    path: "footer-youtube.png"
                },
                {
                    path: "footer-pinterest.png"
                },
                {
                    path: "footer-periscope.png"
                },
            ]       
        };
    }, 
    methods: {
        getImagePath(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }            
    }
}
</script>

<template>
<footer>
    <div class="footer-top">
        <div class="container">
            <!-- Footer Logo -->
            <img src="../assets/img/dc-logo-bg.png" alt="">
            <!-- Footer Links -->
            <div>
                <ul>
                    <h3>DC COMICS</h3>
                    <li v-for="item in comicsItems" :key="item.title"><a href="">{{ item.title }}</a></li>
                </ul>
                <ul>
                    <h3 class="padding-top">SHOP</h3>
                    <li v-for="item in shopItems" :key="item.title"><a href="">{{ item.title }}</a></li>
                </ul>
            </div>
            <div>
                <ul>
                    <h3>DC</h3>
                    <li v-for="item in DcItems" :key="item.title"><a href="">{{ item.title }}</a></li>
                </ul>
            </div>
            <div>
                <ul>
                    <h3>SITES</h3>
                    <li v-for="item in sitesItems" :key="item.title"><a href="">{{ item.title }}</a></li>
                </ul>
            </div>
        </div>        
    </div>
    <div class="footer-bottom">
        <div class="container">
            <button>SIGN-UP NOW!</button>
            <div>
                <h2>FOLLOW US:</h2>
                <ul>
                    <li v-for="img in imgFooter" :key="img.path"><a href=""><img :src="getImagePath(img.path)" alt=""></a></li>
                </ul>
            </div>
        </div>
    </div>
</footer>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
// Footer Top
.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    position: relative;
    padding: 50px;
    z-index: -1;
    .container{
        @include flex(left, start, row);
        gap: 20px;
        
        img{
            position: absolute;
            right: 10%;
            top: -20%;
            z-index: 0;
        }

        h3{
            color: white;
            padding-bottom: 10px;
        }

        .padding-top{
            padding-top: 10px;
        }

        ul {
            list-style: none;
        }

        li {
            padding-bottom: 5px;
        }

        a {
            color: $gray;
            text-decoration: none;
            font-size: 0.8rem;
        }
    }
}
// Footer Bottom
.footer-bottom {
    background-color: $footer-color;
    padding: 40px;
    .container {
        @include flex(space-between, center, row);

        button {
            background-color: transparent;
            font-size: 1.5rem;
            color: white;
            padding: .5rem;
            border: 2px solid $primary;
            &:hover {
                opacity: 50%;
                cursor: pointer
            }
        }

        div {
            @include flex(left, center, row);
            gap: 10px;

            h2 {
                color: $primary
            }

            ul {
                @include flex(left, start, row);
                gap: 10px;
                list-style: none;
            }
        }
    }
}
</style>