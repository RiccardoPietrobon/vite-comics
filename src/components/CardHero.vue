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
        <img :src="singleCard.thumb" alt="">
        <h2>{{ singleCard.series }}</h2>
    </li>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;
</style>