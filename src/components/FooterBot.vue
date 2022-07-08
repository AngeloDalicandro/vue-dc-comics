<template>
    <section>
        <div class="container">
            <div class="sign-up-btn">
                <a :href="signUpBtn.link"> {{ signUpBtn.text }}</a>
            </div>

            <div class="social-links">
                <ul>
                    <li><h2>FOLLOW US</h2></li>
                    <li v-for="socialLink, index in socialLinks" :key="index">
                        <a :href="socialLink.link">
                            <img :src="socialLink.img" :alt="socialLink.name">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "FooterBot",
    data() {
        return {
            signUpBtn: {
                link: "#",
                text: "SIGN UP NOW!"
            },
            socialLinks: [
                {
                    link: "#",
                    img: require("../assets/img/footer-facebook.png"),
                    name: "Facebook"
                },
                {
                    link: "#",
                    img: require("../assets/img/footer-twitter.png"),
                    name: "Twitter"
                },
                                {
                    link: "#",
                    img: require("../assets/img/footer-youtube.png"),
                    name: "Youtube"
                },
                                {
                    link: "#",
                    img: require("../assets/img/footer-pinterest.png"),
                    name: "Pinterest"
                },
                                {
                    link: "#",
                    img: require("../assets/img/footer-facebook.png"),
                    name: "Periscope"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/variables';
section {
    background-color: #303030;
}

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 6rem;

    .sign-up-btn {
        padding: 1rem;
        border: 3px solid $main-color;
        
        a {
            text-decoration: none;
            color: white;
            font-weight: 800;
        }
    }

    .social-links {

        ul {
            list-style-type: none;
            display: flex;
            align-items: center;

            h2 {
                color: $main-color;
                margin-right: 0.5rem;
            }

            li {
                margin: 0 0.5rem;
            }
        }
    }
}

</style>