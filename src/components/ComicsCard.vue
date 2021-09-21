<template>
  <div class="card">
    <img :src="comic.thumb" :alt="comic.series">
    <h3>{{comic.series}}</h3>
  </div>
</template>

<script>
export default {
    name: 'ComicsCard',
    props: ['comic']
}
</script>

<style>
    .card {
        width: calc(100% / 6);
    }
</style>