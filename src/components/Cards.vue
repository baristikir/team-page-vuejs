<template>
  <div v-bind:key="card" v-for="card in cards" class="cards">
    <div class="flex">
      <img v-bind:src="card.profile" alt="profile">
      <div class="vertical-text">
        {{ card.job }}
      </div>
    </div>

    <span class="horizontal-text">
      {{ card.name }}
    </span>
  </div>
</template>

<script>
export default {
  name: 'Cards',
  props: ["cards"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "../scss/variables";
  img{
    width: 238px;
    height: 341px;
  }
  .vertical-text{
    margin-left: 10px;
    font-family: $font-title;
    font-size: $vertical-font;
    writing-mode: vertical-rl;
    text-transform: uppercase;
  }
  .horizontal-text{
    margin-top: 15px;
    font-size: $normal-font;
    font-weight: $semibold;
  }
</style>
