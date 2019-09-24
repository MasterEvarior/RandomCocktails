<template>
        <img v-bind:src="url" class="card-img-top" alt="Ups we could not load the image">
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
   
</style>>
