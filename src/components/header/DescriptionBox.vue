<template>
    <div class="description-box">
        <a href="#">
            <h1 class="title">John Wick 3 : Parabellum</h1>
        </a>
        <div class="rating">
            <div class="imdb">
                <img src="@/assets/imdb-icon.png" alt="imdb">
                <p class="imdb-rate">86.0 / 100</p>
            </div>
            <div class="percentage">
                <img src="@/assets/percentage-icon.png" alt="percentage">
                <p class="percentage-rate">97%</p>
            </div>
        </div>
        <p class="description">
            John Wick is on the run after killing a member of the international assassins' guild, and with a $14 million price tag on his head, he is the target of hit men and women everywhere.
        </p>
        <button class="watch-button">
            <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M10 18C14.4183 18 18 14.4183 18 10C18 5.58172 14.4183 2 10 2C5.58172 2 2 5.58172 2 10C2 14.4183 5.58172 18 10 18ZM9.5547 7.16795C9.24784 6.96338 8.8533 6.94431 8.52814 7.11833C8.20298 7.29235 8 7.63121 8 8V12C8 12.3688 8.20298 12.7077 8.52814 12.8817C8.8533 13.0557 9.24784 13.0366 9.5547 12.8321L12.5547 10.8321C12.8329 10.6466 13 10.3344 13 10C13 9.66565 12.8329 9.35342 12.5547 9.16795L9.5547 7.16795Z" fill="white"/>
            </svg>
            WATCH TRAILER
        </button>
    </div>
</template>

<style scoped>
/* DESCRIPTION BOX */
.description-box {
    width: 400px;
    padding-top: 158px;
    margin-left: 98px;
}

@media screen and (max-width: 650px) {
    .description-box {
        width: 320px;
        margin-left: 38px;
    }
}

/* TITLE */
.title {
    color: #fff;
    font-style: normal;
    font-weight: bold;
    font-size: 48px;
    line-height: 56px;
    margin-bottom: 16px;
}

/* RATING */
.rating {
    display: flex;
    align-items: center;
}

.imdb, 
.percentage {
    display: flex;
    align-items: center;
}

.imdb {
    margin-right: 34px;
}

.imdb img, 
.percentage img {
    margin-right: 10px;
}

.imdb-rate, 
.percentage-rate {
    color: #fff;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 12px;
}

/* DESCRIPTION */
.description {
    color: #fff;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;
    width: 302px;
    margin: 16px 0;
}

/* BUTTON */
.watch-button {
    background-color: #BE123C;
    border: none;
    border-radius: 6px;
    color: #fff;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 24px;
    text-transform: uppercase;
    padding: 6px 16px;
    cursor: pointer;
    display: flex;
    align-items: center;
}

.watch-button svg {
    margin-right: 8px;
}
</style>