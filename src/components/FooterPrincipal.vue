<script>
export default {
    data() {
        return {
            title: "FooterPrincipal",
        };
    },
};
</script>

<template>
    <section class="footer-jumbo">
        <div class="container">
            <div class="listmenu">
                <ul>
                    <h2>DC COMICS</h2>
                    <li>Characters</li>
                    <li>Comics</li>
                    <li>Movies</li>
                    <li>TV</li>
                    <li>Games</li>
                    <li>Videos</li>
                    <li>News</li>

                    <h2>SHOP</h2>
                    <li>Shop DC</li>
                    <li>Shop DC Collectibles</li>
                </ul>
                <ul>
                    <h2>DC COMICS</h2>
                    <li>Terms Of Use</li>
                    <li>Privacy policy (New)</li>
                    <li>Ad Choices</li>
                    <li>Advertising</li>
                    <li>Jobs</li>
                    <li>Subscriptions</li>
                    <li>Talent workshops</li>
                    <li>CPSC Certificates</li>
                    <li>Ratings</li>
                    <li>Shop Help</li>
                    <li>Contact Us</li>
                </ul>

                <ul>
                    <h2>SITES</h2>
                    <li>DC</li>
                    <li>MAD Magazine</li>
                    <li>DC Kids</li>
                    <li>DC Universe</li>
                    <li>DC Power Visa</li>

                </ul>


            </div>
            <div class="dc-logo">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mymixin.scss" as *;

.footer-jumbo {
    background-image: url(../assets/img/footer-bg.jpg);
    max-height: 270px;
}


.dc-logo {
    width: 50%;


    img {
        width: 350px;
        height: 270px;
        object-fit: cover;
    }
}

.listmenu {
    @include flex-left;
    width: 50%;
    padding: 40px 0px;


    ul {
        padding: 0 10px;

        h2 {
            font-weight: bold;
            color: white;
            font-size: 17px;
        }

        li {
            font-size: 10px;
            color: lightgray;

            &:hover {
                cursor: pointer;
                text-decoration: underline;
            }
        }

    }
}
</style>