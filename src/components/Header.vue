<template>
    <div class="header">
        <h1 class="heading">
            {{heading}}
        </h1>
        <div class="header-info">
            <h2 class="header-info__subheading">
                {{subheading}}
            </h2>

            <p class="header-info__content">
                {{content}}
            </p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    heading: String,
    subheading: String,
    content: String,
  }
}
</script>

<style lang="scss">
    @import "../scss/header";
</style>