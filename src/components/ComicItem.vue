<script>
export default {
    name: 'ComicItem',

    props: {
        comicName: String,
        comicImage: String,
    }

}
</script>

<template>
    <div class="comic">
        <div class="comic-image">
            <img :src="comicImage" :alt="comicName">
        </div>
        <h4>{{ comicName }}</h4>
    </div>
</template>

<style lang="scss">
.comic {
    display: flex;
    flex-flow: column;
    align-items: center;

    width: calc(100% / 6 - 27px / 6 * 5);
    gap: 20px;

    .comic-image {
        width: 185px;
        height: 185px;

        overflow: hidden;
        img {
            width: 100%;
        }
    }

}
</style>