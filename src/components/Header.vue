<template>
    <header class="header">
        <Navbar/>
        <DescriptionBox/>
    </header>
</template>

<script>
import Navbar from "./header/Navbar.vue"
import DescriptionBox from "./header/DescriptionBox.vue"
export default {
    components: {
        Navbar,
        DescriptionBox
    }
}
</script>

<style scoped>
/* HEADER */
.header {
    width: 100%;
    max-width: 1440px;
    height: 600px;
    background-image: url("../assets/header-poster.jpg");
    background-origin: border-box;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
}
</style>