<script>
export default {
    name: 'Appnav',

    data() {
        return {
            links: ["Characters", "Comics", "Movies", "TV", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"],

            activeLink: 1,
        }
    },
}
</script>

<template>
    <nav>
        <img id="logo" src="/img/dc-logo.png" alt="">

        <ul>
            <li v-for="(currentLink, index) in links" :class="index == activeLink ? 'active' : ''">
                {{ currentLink }}
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;

    height: 118px;

    #logo {
        width: 80px;
        height: auto;
        padding: 18px;
    }

    ul {
        display: flex;
        justify-content: space-around;
        list-style-type: none;

        padding: 0px 30px;
        gap: 30px;


        li {
            font-weight: bold;
            cursor: pointer;

            text-transform: uppercase;
            padding: 45px 0px;
            color: black;

            &.active {
                color: #0282f9;
                border-bottom: 5px solid #0282f9;
            }
        }
    }
}
</style>