
<script>
export default {
    data() {
        return {
            title: "FOLLOW US",
            social: [
                "footer-facebook.png",
                "footer-periscope.png",
                "footer-pinterest.png",
                "footer-twitter.png",
                "footer-youtube.png",
            ]
        };
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
};
</script>

<template>
    <section class="social">
        <div class="container">
            <div class="left-col">
                <a href="#">SIGN-UP NOW!</a>
            </div>
            <div class="right-col">
                <h2>{{ title }}</h2>
                <ul>
                    <li v-for="pic in social">
                        <img :src="getImagePath(pic)" alt="">
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

.container {
    padding: 40px 0px;
}

.social {
    background-color: $two-color;
}

.left-col {
    width: 50%;
    @include flex-left;

    a {
        text-decoration: none;
        color: white;
        border: 2px solid $one-color;
        padding: 10px;
    }
}

.right-col {
    width: 50%;
    @include flex-right;

    h2 {
        color: $one-color;
    }

    ul {
        @include flex-right;

        li {
            margin: 0 10px;
        }
    }

}
</style>