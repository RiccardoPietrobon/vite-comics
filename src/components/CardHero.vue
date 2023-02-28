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
        <img :src="getImagePath(singleCard.thumb)" alt="superhero">
        <h2>{{ singleCard.series }}</h2>
    </li>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

li {
    padding: 5px;

    width: 15%;

    h2 {
        text-align: left;
        font-size: 14px;
    }
}
</style>