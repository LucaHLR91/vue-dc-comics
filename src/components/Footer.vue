<template>
    <footer>
    
        <div class="footer-top">
            <div class="container">
                <div class="footer-nav">
                    <h3 class="footer-nav-title">DC Comics</h3>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>

                    <h3 class="footer-nav-title">Shop</h3>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>
            <div class="footer-nav">
                <h3 class="footer-nav-title">DC</h3>
                <ul>
                    <li><a href="#">Terms Of Use</a></li>
                    <li><a href="#">Privacy policy(New)</a></li>
                    <li><a href="#">Ad Choices</a></li>
                    <li><a href="#">Advertising</a></li>
                    <li><a href="#">Jobs</a></li>
                    <li><a href="#">Subscription</a></li>
                    <li><a href="#">Talent Workspace</a></li>
                    <li><a href="#">CPSC Certificates</a></li>
                    <li><a href="#">Ratings</a></li>
                    <li><a href="#">Shop Help</a></li>
                    <li><a href="#">Contact US</a></li>
                </ul>
            </div>
            <div class="footer-nav">
                <h3 class="footer-nav-title">Sites</h3>
                <ul>
                    <li><a href="#">DC</a></li>
                    <li><a href="#">MAD Magazine</a></li>
                    <li><a href="#">DC Kids</a></li>
                    <li><a href="#">DC Universe</a></li>
                    <li><a href="#">DC Power Visa</a></li>
                </ul>
            </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
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

    footer {
        background-image: url('../assets/img/footer-bg.jpg');
    }

    .footer-top {
        
        .container {
            display: flex;
        }

        .footer-nav {
            display: flex;
            flex-direction: column;
            

            .footer-nav-title {
                color: white;
                text-transform: uppercase;
            }

            .footer-nav ul li a {
                font-size: 10px;
                color: #537895;
            }
        }
    }

    .footer-bottom {
        height: 100px;
        background-color: #303030;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
    }

    .sign-up-btn {
        padding: 20px;

        button {
            color: white;
            text-transform: uppercase;
            background-color: #303030;
            border: 1px solid $primary;
            padding: 10px 15px;

            &:hover {
                background-color: $primary;
                cursor: pointer;
                box-shadow: #303030;
                transition: 0.3;
            }
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