<script>
export default {
    data() {
        return {
            blueitems: [
                {
                    user: "../assets/img/buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                },
                {
                    user: "../assets/img/buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                },
                {
                    user: "../assets/img/buy-comics-shop-locator.png",
                    text: "SUBSCRIPTION",
                },
                {
                    user: "../assets/img/buy-comics-subscriptions.png",
                    text: "COMIC SHOP LOCATOR",
                },
                {
                    user: "../assets/img/buy-comics-dc-power-visa.svg",
                    text: "DC POWER VISA",
                },
            ],
        };
    },
};
</script>

<template>
    <nav>
        <ul class="container">
            <li v-for="itemblue in blueitems">
                <img :src="itemblue.user" alt="">
                <span>{{ itemblue.text }}</span>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

nav {
    background-color: hsl(209deg 98% 49%);
}

ul {
    @include between;
    padding: 40px 0px;
    color: white;
    font-size: 14px;

    li:hover {
        cursor: pointer;
    }
}
</style>