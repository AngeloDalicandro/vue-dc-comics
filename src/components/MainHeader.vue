<template>
    <header>
        <div class="container">
            <div class="logo-wrapper">
                <img src="../assets/img/dc-logo.png" alt="DC logo">
            </div>

            <nav>
                <ul>
                    <li v-for="navItem, index in navItems" 
                    :key="index" 
                    @click="setActiveElement(index)"
                    >
                    <a :class="{'active': navActiveItem === index}"
                    :href="navItem.link">
                    {{ navItem.name }}
                    </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
import NavItemsData from '../assets/nav-items.json'

export default {
    name: "MainHeader",
    data() {
        return {
            navActiveItem: 1,
            navItems: NavItemsData
        }
    },
    methods: {
        setActiveElement(a) {
            this.navActiveItem = a;
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

header {
    background-color: white;
    height: 8rem;
    
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        line-height: 8rem;
    }  

    .logo-wrapper {
        width: 6rem;
    }
    
    ul { 
        display: flex;
        list-style-type: none;

        li {
            padding: 0 1rem;

            a {
                text-decoration: none;
                color: black;
                display: inline-block;

                &.active {
                    color: $main-color;

                    border-bottom: solid 4px $main-color;
                }
            }
        }
    }
}
</style>
