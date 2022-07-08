<template>
    <div class="footer-top">
        <div class="container">
            <div class="footer-links">

                <div>
                    <ul>
                        <li><h2>DC COMICS</h2></li>
                        <li v-for="dcComicLink, index in dcComicsLinks" :key="index"><a :href="dcComicLink.link">{{ dcComicLink.text }}</a></li>
                    </ul>

                    <ul>
                        <li><h2>Shop</h2></li>
                        <li v-for="shopLink, index in shopLinks" :key="index"><a :href="shopLink.link">{{ shopLink.text }}</a></li>
                    </ul>
                </div>

                <ul>
                    <li><h2>DC</h2></li>
                    <li v-for="dcLink, index in dcLinks" :key="index"><a :href="dcLink.link">{{ dcLink.text }}</a></li>
                </ul>

                <ul>
                    <li><h2>SITES</h2></li>
                    <li v-for="sitesLink, index in sitesLinks" :key="index"><a :href="sitesLink.link">{{ sitesLink.text }}</a></li>
                </ul>
            </div>

            <div class="dc-logo-big">
                <img :src="dcLogoBig" alt="DC logo">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FooterTop",
    data() {
        return {
            dcLogoBig: require("../assets/img/dc-logo-bg.png"),
            dcComicsLinks: [
                {
                    link: "#",
                    text: "Character"
                },
                {
                    link: "#",
                    text: "Comics"
                },
                {
                    link: "#",
                    text: "Movies"
                },
                {
                    link: "#",
                    text: "TV"
                },
                {
                    link: "#",
                    text: "Games"
                },
                {
                    link: "#",
                    text: "Videos"
                },
                {
                    link: "#",
                    text: "News"
                }
            ],
            shopLinks: [
                {
                    link: "#",
                    text: "Shop DC"
                },
                {
                    link: "#",
                    text: "Shop DC Collectibles"
                }
            ],
            dcLinks: [
                {
                    link: "#",
                    text: "Terms of Use"
                },
                {
                    link: "#",
                    text: "Privacy Policy (New)"
                },
                {
                    link: "#",
                    text: "Ad Chioces"
                },
                {
                    link: "#",
                    text: "Advertising"
                },
                {
                    link: "#",
                    text: "Jobs"
                },
                {
                    link: "#",
                    text: "Subscriptions"
                },
                {
                    link: "#",
                    text: "Talent Workshops"
                },
                {
                    link: "#",
                    text: "Ad Chioces"
                },
                {
                    link: "#",
                    text: "CPSC Certificates"
                },
                {
                    link: "#",
                    text: "Ratings"
                },
                {
                    link: "#",
                    text: "Shop Help"
                },
                {
                    link: "#",
                    text: "Contact US"
                }
            ],
            sitesLinks: [
                {
                    link: "#",
                    text: "DC"
                },
                {
                    link: "#",
                    text: "MAD Magazine"
                },
                {
                    link: "#",
                    text: "DC Kids"
                },
                {
                    link: "#",
                    text: "DC Universe"
                },
                {
                    link: "#",
                    text: "DC Power Visa"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/variables';

.footer-top {
    height: 25rem;
    background-image: url('../assets/img/footer-bg.jpg');
    overflow: hidden;
    padding: 2rem;

    .container {
        display: flex;
        flex-wrap: wrap;

        .footer-links {
            width: 60%;
            display: flex;

            ul {
                list-style-type: none;
                color: lightgray;
                margin: 0 2rem 1rem 0;

                h2 {
                    margin-bottom: 1rem;
                    color: white;
                }

                li {
                    margin: 0.25rem 0;
                }

                a {
                    color: inherit;
                    text-decoration: none;
                }
            }
        }

        .dc-logo-big {
            width: 40%;
            position: relative;

            img {
                width: 120%;
                position: absolute;
                top: -5rem;
                right: 0;
            }
        }
    }

}

</style>