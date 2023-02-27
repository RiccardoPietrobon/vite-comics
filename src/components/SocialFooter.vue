
<script>
export default {
    data() {
        return {
            title: "FOLLOW US",
            social: [
                "../assets/img/footer-facebook.png",
                "../assets/img/footer-periscope.png",
                "../assets/img/footer-pinterest.png",
                "../assets/img/footer-twitter.png",
                "../assets/img/footer-youtube.png",
            ]
        };
    },
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
                        <img :src="pic" alt="">
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
    background-color: hsl(0deg 0% 19%);
}

a {
    text-decoration: none;
    color: white;
    border: 2px solid hsl(209deg 98% 49%);
    padding: 10px;
}
</style>