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

<style lang="scss" scoped>
  @import '../style/General';
  @import "../style/Vars";

  .card {
    display: flex;
    flex-direction: column;
    align-items: start;
    width: calc(100% / 6);

    h3 {
      width: 100%;
      color: $titles;
      text-transform: uppercase;
      text-align: start;
      font-size: 12px;
      padding: 10px 0;
    }
  }
</style>