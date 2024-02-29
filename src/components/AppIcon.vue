<script>
export default {
    name: 'AppIcon',

    data() {
        return {
            icons: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    text: 'Digital comics'
                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    text: 'DC merchandise'
                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    text: 'Subscription'
                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    text: 'Comic shop locator'
                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    text: 'DC power visa'
                },

            ],
        }
    },
}
</script>

<template>
    <div id="icon">
        <ul class="list-icon">
            <li v-for="(currentIcon, index) in icons">
                <img :src="currentIcon.image" alt="">
                {{ currentIcon.text }}
            </li>
        </ul>
    </div>
</template>

<style lang="scss">
#icon {
    display: flex;
    height: 155px;

    background-color: #0282f9;
    color: white;

    .list-icon {
        display: flex;

        gap: 120px;

        margin: auto;

        li {
            display: flex;
            align-items: center;

            gap: 10px;

            img {
                width: auto;
                height: 53px;
            }
        }
    }
}
</style>