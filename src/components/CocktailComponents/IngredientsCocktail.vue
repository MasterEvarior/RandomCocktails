<template>
    <div>
        <h2>Ingredients</h2>
        <li>{{ingredients}}</li>
    </div>
</template>

<script>
export default {
    name: "IngredientsCocktail.vue",
    props: {
        "ingredients": Array,
        "amounts": Array
    }
}
</script>

<style scoped>

</style>