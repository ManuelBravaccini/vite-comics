<script>
export default {
    data() {
        return {
            menuItems: [
                {
                    text: "characters",
                    active: false
                },
                {
                    text: "comics",
                    active: true
                },
                {
                    text: "movies",
                    active: false
                },
                {
                    text: "tv",
                    active: false
                },
                {
                    text: "games",
                    active: false
                },
                {
                    text: "collectibles",
                    active: false
                },
                {
                    text: "videos",
                    active: false
                },
                {
                    text: "fans",
                    active: false
                },
                {
                    text: "news",
                    active: false
                },
                {
                    text: "shop",
                    active: false
                }
            ]
        }
    },
}
</script>

<template>
    <header>
        <div class="my-container">
            <nav>
                <div class="main-logo">
                    <img src="../assets/img/dc-logo.png" alt="DC logo">
                </div>
                <ul>
                    <li v-for="menuItem in menuItems" :class="(menuItem.active) ? 'active' : ''">
                        {{ menuItem.text }}
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

header {
    background-color: $header-bg;
}

nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

ul {
    display: flex;
    height: 100%;

    li {
        height: 100%;
        padding: 0 .75rem;
        font-size: .8rem;
        line-height: calc(120px - .45rem);
        text-transform: uppercase;
        font-weight: bold;
    }
}

.active {
    border-bottom: 5px solid $main-color;
    color: $main-color;
}
</style>