<template>
    <nav class="navbar" id="navbar">
        <img src="@/assets/logo.png" alt="logo">
        <div class="search-box">
            <label for="search">
                <svg  id="search-icon" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M14 14L10 10M11.3333 6.66667C11.3333 9.244 9.244 11.3333 6.66667 11.3333C4.08934 11.3333 2 9.244 2 6.66667C2 4.08934 4.08934 2 6.66667 2C9.244 2 11.3333 4.08934 11.3333 6.66667Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </label>
            <input type="search" name="search" id="search" placeholder="What do you want to watch?">
        </div>
        <div class="menu-box">
            <a href="#"><h2 class="sign-in">Sign in</h2></a>
            <svg @click="changeVisibility" id="menu-button" width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="18" cy="18" r="18" fill="#BE123C"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M9.59998 14.4C9.59998 13.7373 10.1372 13.2 10.8 13.2H25.2C25.8627 13.2 26.4 13.7373 26.4 14.4C26.4 15.0628 25.8627 15.6 25.2 15.6H10.8C10.1372 15.6 9.59998 15.0628 9.59998 14.4Z" fill="white"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M9.59998 21.6C9.59998 20.9373 10.1372 20.4 10.8 20.4H25.2C25.8627 20.4 26.4 20.9373 26.4 21.6C26.4 22.2628 25.8627 22.8 25.2 22.8H10.8C10.1372 22.8 9.59998 22.2628 9.59998 21.6Z" fill="white"/>
            </svg>

            <transition name="bounce">
                <HeaderMenu v-if="isShowHeaderMenu"/>
            </transition>

        </div>
    </nav>
</template>

<script>
import HeaderMenu from "./HeaderMenu.vue"
export default {
    data() {
        return {
            isShowHeaderMenu: false
        }
    },
    components: {
        HeaderMenu
    },
    mounted() {
        window.onscroll = () => {
            if (document.body.scrollTop > 80 || document.documentElement.scrollTop > 80) {
                document.getElementById("navbar").style.backgroundColor = "#111827";
            } else {
                document.getElementById("navbar").style.backgroundColor = "transparent";
            }
        }
    },
    methods: {
        changeVisibility() {
            this.isShowHeaderMenu = !this.isShowHeaderMenu
        }
    }
}
</script>

<style scoped>
/* NAVBAR */
.navbar {
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    position: fixed;
    top: 0;
    z-index: 50;
    width: 100%;
    max-width: 1440px;
    background-color: transparent;
    transition: 700ms background-color;
}

/* SEARCH BOX */
.search-box {
    position: relative;
}

#search-icon {
    position: absolute;
    top: 10px;
    right: 10px;
}

#search {
    width: 525px;
    height: 36px;
    color: #fff;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 24px;
    padding: 0 10px;
    border: 2px solid #D1D5DB;
    border-radius: 6px;
    background-color: transparent;
    outline: none;
}

#search::placeholder {
    color: #fff;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 24px;
}

@media screen and (max-width: 900px) {
    .search-box {
        display: none;
    }
}

/* REMOVE (X) ICON FROM SEARCH BAR */
[type="search"]::-webkit-search-cancel-button,
[type="search"]::-webkit-search-decoration {
    -webkit-appearance: none;
    appearance: none;
}

/* MENU BOX */
.menu-box {
    display: flex;
    align-items: center;
}

.sign-in {
    color: #fff;
    font-style: normal;
    font-weight: bold;
    font-size: 16px;
    line-height: 24px;
    margin-right: 27px;
}

@media screen and (max-width: 650px) {
    .sign-in {
        display: none;
    }
}

#menu-button {
    cursor: pointer;
    position: sticky;
    z-index: 50;
}

/* HEADER MENU VUE3 ANIMATION */
.bounce-enter-active {
    animation: bounce-in 0.5s;
}
.bounce-leave-active {
    animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
    0% {
        transform: scale(0);
    }
    50% {
        transform: scale(1.25);
    }
    100% {
        transform: scale(1);
    }
}

</style>