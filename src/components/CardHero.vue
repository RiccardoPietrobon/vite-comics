<script>
export default {
    props: {
        singleCard: Object,
    },
    methods: {
        getImagePath: function (img) {
            return new URL(img, import.meta.url).href;
        }
    }
};
</script>

<template>
    <li>
        <div class="boximg">

            <img :src="getImagePath(singleCard.thumb)" alt="superhero">
            <h2>{{ singleCard.series }}</h2>
        </div>
    </li>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

li {
    padding: 30px;

    width: 15%;

    img {
        width: 200px;
        height: 200px;
        object-fit: cover;
        object-position: top;
    }

    h2 {
        text-align: left;
        font-size: 14px;
        text-transform: uppercase;
        color: white;

        &:hover {
            cursor: pointer;
            text-decoration: underline;
        }
    }
}
</style>