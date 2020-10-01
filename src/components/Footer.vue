<template>
    <footer>
      <span><a href="https://www.brstkr.com">Baris Tikir</a> @ <a href="https://devchallenges.io">DevChallenges</a></span>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style lang="scss">
@import "../scss/variables";
footer{
    position: relative;
    margin-top: 8rem;
    text-align: center;

    > span{
        font-family: $font-footer;
        font-size: $vertical-mobile-font;
        
    }
    > a, a:visited, a:link{
        text-decoration: none;
        font-weight: $bold;
        transition: background-position 275ms ease;
        background: linear-gradient(to right, midnightblue, midnightblue 50%, royalblue 50%);
        background-clip: text;
        background-size: 200% 100%;
        background-position: 100%;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;

        &:hover{
            background-position: 0 100%;
        }
    }
}
</style>