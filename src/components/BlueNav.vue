<script>
export default {
    data() {
        return {
            blueitems: [
                {
                    user: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                },
                {
                    user: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                },
                {
                    user: "buy-comics-shop-locator.png",
                    text: "SUBSCRIPTION",
                },
                {
                    user: "buy-comics-subscriptions.png",
                    text: "COMIC SHOP LOCATOR",
                },
                {
                    user: "buy-comics-dc-power-visa.svg",
                    text: "DC POWER VISA",
                },
            ],
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
    <nav>
        <ul class="container">
            <li v-for="itemblue in blueitems">
                <img :src="getImagePath(itemblue.user)" alt="">

                <span>{{ itemblue.text }}</span>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

nav {
    background-color: $one-color;
}

ul {
    @include between;
    padding: 40px 0px;
    color: white;
    font-size: 14px;

    li {
        @include flex-center;

        span {
            margin: 0 5px;
        }

        img {
            height: 40px;
        }

        &:hover {
            cursor: pointer;
        }
    }
}
</style>