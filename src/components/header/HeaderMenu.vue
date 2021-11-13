<template>
    <div class="header-menu">
                <ul>
                    <li>
                        <a href="#featured-movie">Featured Movie</a>
                    </li>
                    <li>
                        <a href="#new-arrival">New Arrival</a>
                    </li>
                    <li>
                        <a href="#exclusive-videos">Exclusive Videos</a>
                    </li>
                    <li>
                        <a href="#featured-casts">Featured Casts</a>
                    </li>
                    <li>
                        <a href="#">Privacy & Policy</a>
                    </li>
                    <li>
                        <a href="#">About Us</a>
                    </li>
                    <li>
                        <a href="#">Contact</a>
                    </li>
                    <li>
                        <a href="#">Sign up</a>
                    </li>
                </ul>
            </div>
</template>

<style scoped>
/* HEADER MENU */
.header-menu {
    background-color: #BE123C;
    padding: 15px;
    display: inline-block;
    min-width: 150px;
    margin-left: -30px;
    border-radius: 12px;
    position: fixed;
    display: inline-block;
    top: 80px;
    z-index: 50;
}

@media screen and (max-width: 650px) {
    .header-menu {
        margin-left: -110px;
    }
}

.header-menu > ul > li {
    list-style: none;
}

.header-menu > ul > li:not(:last-child) {
    margin-bottom: 10px;
}

.header-menu > ul > li > a {
    color: #fff;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;
}
</style>