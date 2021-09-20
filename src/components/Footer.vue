<template>
    <footer>
        <div class="container">
            <div class="footer-top">

            </div>
            <div class="footer-bottom">
                <div class="sign-up-btn">
                    <button>Sign-up Now!</button>
                </div>
                <div class="social-media-links">
                    <ul>
                        <li><a href="#">Follow Us</a></li>
                        <li><a href="#"></a><img src="../assets/img/footer-facebook.png" alt=""></li>
                        <li><a href="#"></a><img src="../assets/img/footer-twitter.png" alt=""></li>
                        <li><a href="#"></a><img src="../assets/img/footer-youtube.png" alt=""></li>
                        <li><a href="#"></a><img src="../assets/img/footer-pinterest.png" alt=""></li>
                        <li><a href="#"></a><img src="../assets/img/footer-periscope.png" alt=""></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style lang="scss" scoped>
    @import "../style/General";
    @import "../style/Vars";

    .footer-bottom {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100px;
        background-color: #303030;
    }

    .sign-up-btn {
        padding: 20px;

        button {
            color: white;
            text-transform: uppercase;
            background-color: #303030;
            border: 1px solid $primary;
            padding: 10px 15px;
        }
    }

    .social-media-links ul:first-child a {
        color: $primary;
        font-weight: bold;
    }

    .social-media-links ul {
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 10px 15px;

        li {
            padding: 10px 10px;
        }
    }
</style>