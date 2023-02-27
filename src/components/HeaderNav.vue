<script>
export default {
    data() {
        return {
            items: [
                "CHARACTERS",
                "COMICS",
                "MOVIES",
                "TV",
                "GAMES",
                "COLLECTIBLES",
                "VIDEOS",
                "FANS",
                "NEWS",
                "SHOP",
            ]
        };
    },
};
</script>

<template>
    <header>
        <nav class="container">
            <!-- logo dc -->
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="DC_logo">
            </div>
            <!-- items navbar -->
            <ul>
                <li v-for="item in items">{{ item }}</li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

.container {
    @include between;
}

ul {
    @include flex-center;

    li {
        margin: 0 10px;
        padding: 70px 0px;
        font-weight: bold;
        font-size: 12px;

        &:hover {
            color: var(--one-color);
            border-bottom: 4px solid var(--one-color);
            cursor: pointer;
        }
    }
}

.logo,
ul {
    width: 50%;
}
</style>