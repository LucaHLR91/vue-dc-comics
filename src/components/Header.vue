<template>
    <header>
        <div class="black-bar"></div>
        <div class="container">
            <div id="logo">
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>
            <div class="list">
                <ul>
                    <li v-for="(link, index) in links" :key="index"><a :class="(link.current) ? 'active' : null" :href="link.url">{{ link.text }}</a></li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import "../style/General";
    @import "../style/Vars";

    header {
        .black-bar {
            height: 30px;
            background-color: #000;
        }

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            #logo {
                padding: 20px;
            }

            .list {
                height: 100%;
            }
        }

        ul {
            display: flex;
            justify-content: space-around;
            align-items: center;

            li a {
                padding: 1rem;
                font-weight: 600;
                font-size: 12px;
                transition: 0.3;
                
                &:hover,
                &.active {
                    color: $primary;
                    border-bottom: 2px solid $primary;
                    
                }
            }
        }
    }

</style>