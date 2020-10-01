<template>
<!-- Card Deck-->
<div class="cards">
  <!-- Iteration through all available Card Objects -->
  <div v-bind:key="card" v-for="card in cards" class="card">
      <!-- Helper Class - Flexbox -->
      <div class="flex">
        <!-- Profile Image -->
        <img v-bind:src="card.profile" alt="profile">
        <!-- Vertical Job Text-->
        <div class="vertical-text">
          {{ card.job }}
        </div>
      </div>
      <!-- Profile Name -->
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

<style lang="scss">
@import "../scss/variables";
@import "../scss/mixins";
.cards{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
  padding-top: 12px;
}
.card{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding-top: 42px;

  &:nth-child(3n + 2){
    transform: translateY(0px);
    @include breakpoint('s'){
      transform: translateY(58px);
    }
    @include breakpoint('m'){
      transform: translateY(150px);
    }
  }

  &:nth-child(2n + 0){
      transform: translateY(58px);
    @include breakpoint('s'){
      transform: translateY(45px)
    }
    @include breakpoint('m'){
      transform: translateY(80px)
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
    font-size: $vertical-mobile-font;
    vertical-align: top;
    writing-mode: vertical-rl;
    text-transform: uppercase;

    @include breakpoint('s'){
      font-size: $vertical-font;
    }
  }

  .horizontal-text{
    margin-top: 15px;
    font-size: $normal-mobile-font;
    font-weight: $semibold;
    display: inline-block;
    text-align: left;

    @include breakpoint('s'){
      font-size: $normal-font;
    }
  }
}
</style>
