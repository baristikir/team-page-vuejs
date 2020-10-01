<template>
<div class="cards">
  <div v-bind:key="card" v-for="card in cards" class="card">
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
@import "../scss/mixins";
.cards{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
  padding-top: 52px;
}
.card{
  align-items: flex-start;

  &:nth-child(2n){
    padding-top: 58px;
    @include breakpoint('s'){
      padding-top: 100px;
    }
  }
  &:nth-child(5){
    padding-top: 0px;
    @include breakpoint('s'){
      padding-top: 100px;
    }
  }

  img{
      width: 138px;
      height: 208px;
    @include breakpoint('s'){
      width: 238px;
      height: 341px;
    }
  }

  .vertical-text{
    margin-left: 10px;
    font-family: $font-title;
    font-size: $vertical-font;
    vertical-align: top;
    writing-mode: vertical-rl;
    text-transform: uppercase;
  }

  .horizontal-text{
    margin-top: 15px;
    font-size: $normal-font;
    font-weight: $semibold;
    display: inline-block;
    text-align: left;
  }
}
</style>
