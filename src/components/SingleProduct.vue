<template>
    <div class="comic-card">

        <div class="image-container">
            <img :src="img" :alt="name">
        </div>

        <div class="comic-name"> {{ name.toUpperCase() }} </div>

    </div>
</template>

<script>
export default {
    name: "SingleProduct",
    props: {
        img: String,
        name: String
    }
}
</script>

<style lang="scss" scoped>

@import '../styles/variables';

.comic-card {
    margin: 0.75rem;
    width: 12rem;

    .image-container {
        height: 12rem;
        overflow: hidden;
    }

    .comic-name {
        color: white;
        text-overflow: hidden;
        line-break: auto;
        margin: 1rem 0;
    }

}
</style>