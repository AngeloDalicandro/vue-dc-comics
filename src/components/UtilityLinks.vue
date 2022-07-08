<template>
    <section>
        <div class=container>
            <UtilityItem v-for="item, index in items" :key="index"
            :img="item.img"
            :text="item.text" 
            />
        </div>
    </section>

</template>

<script>
import UtilityItem from './UtilityItem.vue';

export default {
    name: 'UtilityLinks',
    components: {
        UtilityItem
    },
    data() {
        return {
            items: [
                {
                    img: require("../assets/img/buy-comics-digital-comics.png"),
                    text: "DIGITAL COMICS"
                },
                {
                    img: require("../assets/img/buy-comics-merchandise.png"),
                    text: "DC MERCHANDISE"
                },
                {
                    img: require("@/assets/img/buy-comics-subscriptions.png"),
                    text: "SUBSCRIPTION"
                },
                {
                    img: require("@/assets/img/buy-comics-shop-locator.png"),
                    text: "COMIC SHOP LOCATOR"
                },
                {
                    img: require("@/assets/img/buy-dc-power-visa.svg"),
                    text: "DC POWER VISA"
                }
            ]
        }
    }
}
</script>

<style lang=scss scoped>
@import '../styles/variables';

section {
    background-color: $main-color;
    height: 10rem;

    .container {
        display: flex;
        justify-content: space-between;
        line-height: 10rem;
    }
}
</style>