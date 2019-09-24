<template>
    <div>
        <img v-bind:src="url" class="card-img-top" alt="Ups we could not load the image">
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
        height: 25em;
        width: 25em;
    } 
</style>>
