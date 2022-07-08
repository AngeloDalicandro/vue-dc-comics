<template>
    <div class="jumbotron">
        <div class="container">
            <div>CURRENT SERIES</div>
        </div>
    </div>
</template>

<script>
export default {
    name: "DcJumbo"
}
</script>

<style lang="scss" scoped>
@import '../styles/variables';

.jumbotron {
    background-image: url('../assets/img/jumbotron.jpg');
    background-repeat: no-repeat;
    height: 25rem;

    .container {
        position: relative;
        height: 100%;

        div {
            background-color: $main-color;
            display: inline-block;
            padding: 0.5rem 1rem;
            font-size: 2rem;
            color: white;
            position: absolute;
            left: 0;
            top: 100%;
            transform: translate(0, -50%);
        }
    }


}

</style>