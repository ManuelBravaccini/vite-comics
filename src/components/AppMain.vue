<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<template>
    <main>
        <div class="my-container">
            <h1>Content goes here</h1>
        </div>
    </main>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;

main {
    background-color: $main-dark-bg;
    color: white;
    height: 150px;

    div.my-container {
        display: flex;
        height: 100%;
        align-items: center;
    }
}
</style>