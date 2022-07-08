<template>
    <div class="utility-item">
        
        <img :src="img" :alt="text">

        <span>{{text}}</span>

    </div>
</template>

<script>
export default {
    name: "UtilityItem",
    props: {
        img: String,
        text: String
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/variables';

.utility-item {
    color: white;
    display: flex;
    align-items: center;

    img {
        color: white;
        width: 3rem;
        margin-right: 1rem;
    }
}

</style>