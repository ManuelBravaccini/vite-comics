<script>
export default {
    props: {
        comic: Object
    },
}
</script>

<template>
    <article class="comic-card">
        <img :src="comic.thumb" alt="comic.series">
        <h3>
            {{ comic.series }}
        </h3>
    </article>
</template>

<style lang="scss" scoped>
article {
    display: flex;
    flex-direction: column;
    width: calc(100% / 6);
    padding: 1rem;
    text-align: center;


    img {
        height: 60%;
        object-fit: cover;
        object-position: top;
        margin-bottom: .5rem;
    }

}
</style>