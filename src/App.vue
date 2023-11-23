<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"

export default {
    components: {
    AppHeader,
    AppMain,
    AppFooter,
},
}
</script>

<template>
<AppHeader/>
</template>

<style lang="scss">
@use "./style/general.scss";

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

img {
    max-width: 100%;
}

body {
    font-family: Arial, Helvetica, sans-serif;
}
</style>
