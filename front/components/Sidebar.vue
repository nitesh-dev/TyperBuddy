<script setup lang='ts'>
defineProps({
    activeTabIndex: Number
})

</script>
<template>
    <div class="sidebar-container">
        <nav class="sidebar">
            <div class="heading">
                <img src="../public/favicon.ico" alt="TyperBuddy">
                <h2>TyperBuddy</h2>
            </div>
            <hr>
            <ul>
                <li :class="{ 'active': activeTabIndex == 0 }">
                    <NuxtLink to="/">
                        <span class="marker"></span>
                        <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M21.25 19.5a.75.75 0 0 1 .102 1.493L21.25 21H2.75a.75.75 0 0 1-.102-1.493l.102-.007h18.5ZM19.745 3a2.25 2.25 0 0 1 2.25 2.25v9.505a2.25 2.25 0 0 1-2.25 2.25h-6.521a1.25 1.25 0 0 1-2.448 0H4.25A2.25 2.25 0 0 1 2 14.755V5.25A2.25 2.25 0 0 1 4.25 3h15.495Zm0 1.5H4.25a.75.75 0 0 0-.75.75v9.505c0 .414.336.75.75.75h15.495a.75.75 0 0 0 .75-.75V5.25a.75.75 0 0 0-.75-.75Zm-2.495 8a.75.75 0 0 1 .102 1.493L17.25 14H6.75a.75.75 0 0 1-.102-1.493l.102-.007h10.5ZM16.5 9a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm-5.995 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm-3 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm6 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2ZM6 6a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm2.995 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm3 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm3 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm3 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2Z" />
                        </svg>
                        <p>Practice</p>
                    </NuxtLink>

                </li>

                <li :class="{ 'active': activeTabIndex == 1 }">
                    <NuxtLink to="/statistics">
                        <span class="marker"></span>
                        <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M16.749 2h4.554l.1.014.099.028.06.026c.08.034.153.085.219.15l.04.044.044.057.054.09.039.09.019.064.014.064.009.095v4.532a.75.75 0 0 1-1.493.102l-.007-.102V4.559l-6.44 6.44a.75.75 0 0 1-.976.073L13 11 9.97 8.09l-5.69 5.689a.75.75 0 0 1-1.133-.977l.073-.084 6.22-6.22a.75.75 0 0 1 .976-.072l.084.072 3.03 2.91L19.438 3.5h-2.69a.75.75 0 0 1-.742-.648l-.007-.102a.75.75 0 0 1 .648-.743L16.75 2ZM3.75 17a.75.75 0 0 1 .75.75v3.5a.75.75 0 0 1-1.5 0v-3.5a.75.75 0 0 1 .75-.75Zm5.75-3.25a.75.75 0 0 0-1.5 0v7.5a.75.75 0 0 0 1.5 0v-7.5ZM13.75 15a.75.75 0 0 1 .75.75v5.5a.75.75 0 0 1-1.5 0v-5.5a.75.75 0 0 1 .75-.75Zm5.75-4.25a.75.75 0 0 0-1.5 0v10.5a.75.75 0 0 0 1.5 0v-10.5Z" />
                        </svg>
                        <p>Statistics</p>
                    </NuxtLink>

                </li>

                <li :class="{ 'active': activeTabIndex == 2 }">
                    <NuxtLink to="/typing-test">
                        <span class="marker"></span>
                        <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="m10.05 15.42 6.256-8.475a.694.694 0 0 1 1.235.57l-.03.098-3.87 9.799a2.07 2.07 0 1 1-3.737-1.765l.069-.116.076-.11 6.257-8.476-6.257 8.476Zm3.8-2.622-2.594 3.514-.04.062a.57.57 0 0 0 .222.776l.067.032a.57.57 0 0 0 .7-.238l.04-.083 1.605-4.063Zm4.76-5.384a10.66 10.66 0 0 1 2.022 2.172c.524.749 1.03 1.656 1.32 2.398a.75.75 0 1 1-1.397.547 8.238 8.238 0 0 0-.378-.812l-2.05 1.183a.75.75 0 0 1-.834-1.242l.085-.057 2.018-1.166-.23-.314a9.156 9.156 0 0 0-1.058-1.16l.38-.964c.038-.096.067-.194.087-.292l.024-.147.01-.146Zm-2.63-1.561a1.715 1.715 0 0 0-.406.328l-.114.14-.54.733a9.205 9.205 0 0 0-2.17-.47v2.672a.75.75 0 0 1-1.493.102l-.007-.102v-2.69A9.108 9.108 0 0 0 6.658 8.2c-.816.572-1.528 1.322-2.119 2.205l2.082 1.202a.75.75 0 0 1-.658 1.344l-.092-.045-2.074-1.197c-.128.266-.246.54-.356.821a.75.75 0 0 1-1.398-.543c.807-2.075 2.08-3.843 3.754-5.016a10.642 10.642 0 0 1 10.183-1.117Z" />
                        </svg>
                        <p>Typing Test</p>
                    </NuxtLink>
                </li>

                <li :class="{ 'active': activeTabIndex == 3 }">
                    <NuxtLink to="/multiplayer">
                        <span class="marker"></span>
                        <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M2.75 4a.75.75 0 0 0 0 1.5h1.14a1.75 1.75 0 0 1 1.676 1.247L6.242 9H2.75a.75.75 0 0 0 0 1.5h4c.966 0 1.75.784 1.75 1.75v2.5c0 .281-.093.54-.25.75a3.251 3.251 0 1 0 .217 1.717A2.75 2.75 0 0 0 10 14.75v-2.5a3.251 3.251 0 0 0-2.133-3.053l-.864-2.88A3.25 3.25 0 0 0 3.89 4H2.75Zm.75 12.75a1.75 1.75 0 1 1 3.5 0 1.75 1.75 0 0 1-3.5 0Zm16.165-10.4a1.75 1.75 0 0 1 1.5-.85h.085a.75.75 0 0 0 0-1.5h-.084a3.25 3.25 0 0 0-2.787 1.578l-2.15 3.583-2.799 1.244a3.25 3.25 0 0 0-1.93 2.97v1.375a2.75 2.75 0 0 0 2.586 2.745 3.251 3.251 0 0 0 6.327.005h.837a.75.75 0 0 0 0-1.5h-.837a3.251 3.251 0 0 0-6.324-.01A1.25 1.25 0 0 1 13 14.75v-1.375a1.75 1.75 0 0 1 1.04-1.6l2.87-1.275h4.34a.75.75 0 0 0 0-1.5h-3.175l1.59-2.65ZM15.5 16.75a1.75 1.75 0 1 1 3.5 0 1.75 1.75 0 0 1-3.5 0ZM10.25 5a.75.75 0 0 1 .75.75v2a.75.75 0 0 1-1.5 0v-2a.75.75 0 0 1 .75-.75Zm4.1 2.7a.75.75 0 1 0-1.2-.9l-1.5 2a.75.75 0 1 0 1.2.9l1.5-2Z" />
                        </svg>
                        <p>Multiplayer</p>
                    </NuxtLink>
                </li>

                <li :class="{ 'active': activeTabIndex == 4 }">
                    <NuxtLink to="/play-with-friends">
                        <span class="marker"></span>
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M2 8.5C2.00025 9.95312 2.48718 11.3643 3.38311 12.5083C4.27903 13.6524 5.53232 14.4634 6.943 14.812C6.9745 13.0655 7.57723 11.3775 8.659 10.006C8.344 9.9801 8.02735 10.0295 7.73523 10.1502C7.44311 10.2709 7.18389 10.4593 6.979 10.7C6.91498 10.7749 6.83685 10.8364 6.74905 10.881C6.66126 10.9257 6.56554 10.9526 6.46734 10.9603C6.36914 10.9679 6.27039 10.9562 6.17674 10.9257C6.08309 10.8952 5.99636 10.8465 5.9215 10.7825C5.77033 10.6532 5.67671 10.4692 5.66124 10.2708C5.64576 10.0725 5.70971 9.87618 5.839 9.725C6.32185 9.16005 6.97199 8.76346 7.69528 8.59266C8.41856 8.42186 9.17744 8.48573 9.862 8.775C11.257 7.62159 13.0022 6.97571 14.812 6.943C14.4326 5.39999 13.5012 4.04938 12.1937 3.14644C10.8862 2.2435 9.29322 1.85076 7.71585 2.04245C6.13848 2.23415 4.68596 2.99699 3.63279 4.18681C2.57963 5.37664 1.99877 6.91103 2 8.5ZM7.5 6.5C7.5 6.76522 7.39464 7.01957 7.20711 7.20711C7.01957 7.39465 6.76522 7.5 6.5 7.5C6.23479 7.5 5.98043 7.39465 5.7929 7.20711C5.60536 7.01957 5.5 6.76522 5.5 6.5C5.5 6.23479 5.60536 5.98043 5.7929 5.7929C5.98043 5.60536 6.23479 5.5 6.5 5.5C6.76522 5.5 7.01957 5.60536 7.20711 5.7929C7.39464 5.98043 7.5 6.23479 7.5 6.5ZM11.5 6.5C11.5 6.76522 11.3946 7.01957 11.2071 7.20711C11.0196 7.39465 10.7652 7.5 10.5 7.5C10.2348 7.5 9.98043 7.39465 9.7929 7.20711C9.60536 7.01957 9.5 6.76522 9.5 6.5C9.5 6.23479 9.60536 5.98043 9.7929 5.7929C9.98043 5.60536 10.2348 5.5 10.5 5.5C10.7652 5.5 11.0196 5.60536 11.2071 5.7929C11.3946 5.98043 11.5 6.23479 11.5 6.5ZM22 15C22 16.8565 21.2625 18.637 19.9497 19.9498C18.637 21.2625 16.8565 22 15 22C13.1435 22 11.363 21.2625 10.0503 19.9498C8.7375 18.637 8 16.8565 8 15C8 13.1435 8.7375 11.363 10.0503 10.0503C11.363 8.7375 13.1435 8 15 8C16.8565 8 18.637 8.7375 19.9497 10.0503C21.2625 11.363 22 13.1435 22 15ZM13.5 13.5C13.5 13.2348 13.3946 12.9804 13.2071 12.7929C13.0196 12.6054 12.7652 12.5 12.5 12.5C12.2348 12.5 11.9804 12.6054 11.7929 12.7929C11.6054 12.9804 11.5 13.2348 11.5 13.5C11.5 13.7652 11.6054 14.0196 11.7929 14.2071C11.9804 14.3946 12.2348 14.5 12.5 14.5C12.7652 14.5 13.0196 14.3946 13.2071 14.2071C13.3946 14.0196 13.5 13.7652 13.5 13.5ZM17.971 16.718C17.8449 16.6108 17.6815 16.5579 17.5165 16.5711C17.3516 16.5842 17.1985 16.6622 17.091 16.788C16.833 17.0897 16.5128 17.3321 16.1523 17.4983C15.7919 17.6645 15.3997 17.7508 15.0027 17.751C14.6057 17.7513 14.2134 17.6657 13.8527 17.4999C13.492 17.3342 13.1714 17.0924 12.913 16.791C12.8604 16.7261 12.7953 16.6725 12.7215 16.6332C12.6478 16.594 12.5669 16.5699 12.4837 16.5624C12.4005 16.5549 12.3167 16.5642 12.2371 16.5896C12.1576 16.6151 12.0839 16.6563 12.0206 16.7107C11.9572 16.7651 11.9054 16.8317 11.8682 16.9065C11.8309 16.9812 11.8091 17.0627 11.8039 17.1461C11.7987 17.2295 11.8103 17.313 11.838 17.3919C11.8657 17.4707 11.9088 17.5432 11.965 17.605C12.3408 18.0432 12.807 18.3948 13.3315 18.6357C13.8561 18.8766 14.4266 19.001 15.0039 19.0005C15.5811 18.9999 16.1514 18.8743 16.6755 18.6324C17.1996 18.3905 17.6651 18.0379 18.04 17.599C18.1473 17.4731 18.2003 17.3097 18.1874 17.1447C18.1745 16.9798 18.0967 16.8257 17.971 16.718ZM17.5 14.5C17.7652 14.5 18.0196 14.3946 18.2071 14.2071C18.3946 14.0196 18.5 13.7652 18.5 13.5C18.5 13.2348 18.3946 12.9804 18.2071 12.7929C18.0196 12.6054 17.7652 12.5 17.5 12.5C17.2348 12.5 16.9804 12.6054 16.7929 12.7929C16.6054 12.9804 16.5 13.2348 16.5 13.5C16.5 13.7652 16.6054 14.0196 16.7929 14.2071C16.9804 14.3946 17.2348 14.5 17.5 14.5Z" />
                        </svg>

                        <p>Play with Friends</p>
                    </NuxtLink>
                </li>

                <li :class="{ 'active': activeTabIndex == 5 }">
                    <NuxtLink to="/help">
                        <span class="marker"></span>
                        <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M12 2c5.523 0 10 4.477 10 10s-4.477 10-10 10a9.96 9.96 0 0 1-4.587-1.112l-3.826 1.067a1.25 1.25 0 0 1-1.54-1.54l1.068-3.823A9.96 9.96 0 0 1 2 12C2 6.477 6.477 2 12 2Zm0 1.5A8.5 8.5 0 0 0 3.5 12c0 1.47.373 2.883 1.073 4.137l.15.27-1.112 3.984 3.987-1.112.27.15A8.5 8.5 0 1 0 12 3.5Zm0 12a1 1 0 1 1 0 2 1 1 0 0 1 0-2Zm0-8.75a2.75 2.75 0 0 1 2.75 2.75c0 1.01-.297 1.574-1.051 2.359l-.169.171c-.622.622-.78.886-.78 1.47a.75.75 0 0 1-1.5 0c0-1.01.297-1.574 1.051-2.359l.169-.171c.622-.622.78-.886.78-1.47a1.25 1.25 0 0 0-2.493-.128l-.007.128a.75.75 0 0 1-1.5 0A2.75 2.75 0 0 1 12 6.75Z" />
                        </svg>
                        <p>Help</p>
                    </NuxtLink>
                </li>

                <li :class="{ 'active': activeTabIndex == 6 }">
                    <NuxtLink to="/settings">
                        <span class="marker"></span>
                        <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M12.012 2.25c.734.008 1.465.093 2.182.253a.75.75 0 0 1 .582.649l.17 1.527a1.384 1.384 0 0 0 1.927 1.116l1.401-.615a.75.75 0 0 1 .85.174 9.792 9.792 0 0 1 2.204 3.792.75.75 0 0 1-.271.825l-1.242.916a1.381 1.381 0 0 0 0 2.226l1.243.915a.75.75 0 0 1 .272.826 9.797 9.797 0 0 1-2.204 3.792.75.75 0 0 1-.848.175l-1.407-.617a1.38 1.38 0 0 0-1.926 1.114l-.169 1.526a.75.75 0 0 1-.572.647 9.518 9.518 0 0 1-4.406 0 .75.75 0 0 1-.572-.647l-.168-1.524a1.382 1.382 0 0 0-1.926-1.11l-1.406.616a.75.75 0 0 1-.849-.175 9.798 9.798 0 0 1-2.204-3.796.75.75 0 0 1 .272-.826l1.243-.916a1.38 1.38 0 0 0 0-2.226l-1.243-.914a.75.75 0 0 1-.271-.826 9.793 9.793 0 0 1 2.204-3.792.75.75 0 0 1 .85-.174l1.4.615a1.387 1.387 0 0 0 1.93-1.118l.17-1.526a.75.75 0 0 1 .583-.65c.717-.159 1.45-.243 2.201-.252Zm0 1.5a9.135 9.135 0 0 0-1.354.117l-.109.977A2.886 2.886 0 0 1 6.525 7.17l-.898-.394a8.293 8.293 0 0 0-1.348 2.317l.798.587a2.881 2.881 0 0 1 0 4.643l-.799.588c.32.842.776 1.626 1.348 2.322l.905-.397a2.882 2.882 0 0 1 4.017 2.318l.11.984c.889.15 1.798.15 2.687 0l.11-.984a2.881 2.881 0 0 1 4.018-2.322l.905.396a8.296 8.296 0 0 0 1.347-2.318l-.798-.588a2.881 2.881 0 0 1 0-4.643l.796-.587a8.293 8.293 0 0 0-1.348-2.317l-.896.393a2.884 2.884 0 0 1-4.023-2.324l-.11-.976a8.988 8.988 0 0 0-1.333-.117ZM12 8.25a3.75 3.75 0 1 1 0 7.5 3.75 3.75 0 0 1 0-7.5Zm0 1.5a2.25 2.25 0 1 0 0 4.5 2.25 2.25 0 0 0 0-4.5Z" />
                        </svg>
                        <p>Settings</p>
                    </NuxtLink>
                </li>

            </ul>
        </nav>
    </div>
</template>
<style scoped>
/*  ------------------- side bar----------------- */

.sidebar-container{
    width: 300px;
}
.sidebar {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 5;
    width: inherit;
    padding: var(--page-margin) 0;
    height: 100vh;
    background-color: var(--color-surface-variant);
}


.heading {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 1em;
    margin: 0 1rem;
}

.sidebar hr {
    margin: 1rem 0.6rem;
    border: none;
    border-top: 1px solid var(--color-surface-dark);
}

.sidebar ul {
    list-style-type: none;
    padding: 0;
}

.sidebar li {
    padding: 0;
    padding: 0.8rem 2rem;
    position: relative;
    color: var(--color-primary);
}

.sidebar li a {
    display: flex;
    gap: 0.6rem;
    align-items: center;
    color: inherit;
    text-decoration: none;
}


.sidebar li .marker {
    width: 6px;
    background-color: var(--color-primary);
    height: 0;
    position: absolute;
    left: -6px;
    top: 50%;
    border-top-right-radius: 8px;
    border-bottom-right-radius: 8px;
    translate: 0 -50%;
    transition: all 200ms;
}

.sidebar li svg {
    fill: var(--color-primary);
}

.sidebar li.active .marker {
    height: 80%;
    left: 0;
    background-color: var(--color-secondary);
}

.sidebar li.active {
    background-color: var(--color-secondary-light) !important;
    color: var(--color-secondary);
}

.sidebar li:hover {
    background-color: var(--color-primary-light);
}

.sidebar li:hover .marker {
    left: 0;
    height: 80%;
}

.sidebar li.active svg {
    fill: var(--color-secondary);
}


@media only screen and (max-width: 1200px) {
    .sidebar li {
        padding: 0.8rem 1rem;
    }

    .heading h2 {
        font-size: var(--average-font);
    }
    .sidebar-container{
        width: 220px;
    }

}

@media only screen and (max-width: 900px) {

    .sidebar{
        left: -300px;
        width: 300px;
        background-color: var(--color-surface-variant);
    }

}


</style>