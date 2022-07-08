<template>
    <section>

        <div class="container">
            <singleProduct
             v-for="comic, index in comics"
             :key="index"
             :img="comic.thumb"
             :name="comic.series"
              />
        </div>
            
        <div class="btn">LOAD MORE</div>    
    </section>
</template>

<script>
import dcComics from '../assets/dc-comics.json';
import singleProduct from './SingleProduct.vue';

export default {
    name: "ProductsSection",
    components: {
        singleProduct
    },
    data() {
        return {
            comics: dcComics
        }
    }
}
</script>

<style lang="scss" scoped>

@import '../styles/variables';

section {
    padding: 4rem 0 2rem 0;
    background-color: #1c1c1c;
    text-align: center;

    .container {
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
    }    

    .btn {
        display: inline-block;
        background-color: $main-color;
        color: white;
        padding: 0.5rem 3rem;
        cursor: pointer;
    }
}
</style>