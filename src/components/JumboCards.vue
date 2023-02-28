<script>

import CardHero from './CardHero.vue';

export default {
    props: {
        arrayCards: Array,
    },

    components: { CardHero },
};
</script>

<template>
    <img src="../assets/img/jumbotron.jpg" alt="">
    <section class="cards-section">
        <div class="container">
            <a href=""></a>
            <ul>
                <!-- ciclo e faccio passare singleCard ovvero l'oggetto con tutti i suoi parametri -->
                <CardHero v-for="card in arrayCards" :singleCard="card" />
            </ul>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

.cards-section {
    background-color: $three-color;
}

img {
    height: 400px;
    width: 100%;
    object-fit: cover;
    object-position: top;
}

ul {
    display: flex;
    flex-wrap: wrap;
}
</style>