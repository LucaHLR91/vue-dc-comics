<template>
    <main>
        <div class="main-comics">
            <ComicsCard  v-for="(card, index) in Cards" :key="index" :comic='card' />
        </div>
        <div class="main-links">
            <div class="link" v-for="(link, index) in MainLinks" :key="index" >
                <img :src="link.src" :alt="link.text">
                <span>{{link.text}}</span>
            </div>
        </div>
        <div class="main-button">
            <button>Load More</button>
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
        }

        .main-links {
            display: flex;
            justify-content: space-around;
            align-items: center;
            background-color: $primary;
        }

        .main-button {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 10px 15px;

            button {
                padding: 10px 50px;
                background-color: $primary;
                color: white;
                font-weight: bold;
                text-transform: uppercase;
                border: none;
            }
        }
    }
</style>