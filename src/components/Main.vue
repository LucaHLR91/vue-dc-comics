<template>
    <main>
        <div class="main-comics">
            <ComicsCard  v-for="(card, index) in Cards" :key="index" :comic='card' />
        </div>
        <div class="main-button">
            <button>Load More</button>
        </div>
        <div class="main-links">
            <div class="container">
            <div class="link" v-for="(link, index) in MainLinks" :key="index" >
                <img :src="require(`../${link.src}`)" :alt="link.text">
                <span>{{link.text}}</span>
            </div>
            </div>
        </div>
        
    </main>
</template>

<script>
import ComicsCard from './ComicsCard.vue'
import data from '../data/dc-comics.json'
import mainLinks from '../data/mainLink'

export default {
    name: 'Main',
    components: {
        ComicsCard
    },
    data() {
        return {
            Cards: data,
            MainLinks: mainLinks
        }
    }
}
</script>

<style lang="scss" scoped>
    @import "../style/General";
    @import "../style/Vars";

    main {
        background-color: black;

        .main-comics {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            align-items: center;
            width: 70%;
            margin: 0 auto;
            padding: 40px;          
        }

        .main-button {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 15px 15px;

            button {
                padding: 10px 50px;
                background-color: $primary;
                color: $titles;
                font-weight: bold;
                text-transform: uppercase;
                border: none;
                cursor: pointer;
            }
        }

        .main-links {
            padding: 20px;
            background-color: $primary;

            .container {
                display: flex;
                justify-content: space-around;
                align-items: center;
            }

            .link {
                display: flex;
                align-items: center;
                width: 100px;
                height: 100px;

                img {
                    width: 50%;
                }

                span {
                    color: $titles;
                    font-size: 12px;
                    font-weight: bold;
                    text-transform: uppercase;
                    margin-left: 15px;
                }
                
            }
        }
    }
</style>