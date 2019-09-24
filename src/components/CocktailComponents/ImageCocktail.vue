<template>
    <div>
        <img v-bind:src="url" alt="Ups we could not load the image">
    </div>
</template>

<script>
export default {
    name: "ImageCocktail",
    props: {
        url: String
    }
}
</script>

<style scoped>
    img {
        border: 0.1em white solid;
        border-radius: 50%;
        height: 15em;
        width: 15em;
    }
</style>>
