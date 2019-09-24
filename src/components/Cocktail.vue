<template>
    <div>
        <div v-bind:key="cocktail.id" v-for="cocktail in cocktails">
            <h1>{{cocktail.strDrink}}</h1>
            <ImageCocktail v-bind:url="cocktail.strDrinkThumb"/>
            <InstructionsCocktail v-bind:instructions="cocktail.strInstructions"/>
            <IngredientsCocktail v-bind:ingredients="getIngredients"/>
        </div>
    </div>
</template>

<script>
import ImageCocktail from "./CocktailComponents/ImageCocktail";
import InstructionsCocktail from "./CocktailComponents/InstructionsCocktail";
import IngredientsCocktail from "./CocktailComponents/IngredientsCocktail";

export default {
    name: "Cocktail",
    props: ["cocktails"],
    components: {
        ImageCocktail,
        InstructionsCocktail,
        IngredientsCocktail
    },
    methods: {
        getIngredients(cocktail) {
            var array;
            if(cocktail.strIngredient1 !== null && cocktail.strIngredient1 !== "" && cocktail.strIngredient1 !== ''){
                array.push(cocktail.strIngredient1)
            }
            if(cocktail.strIngredient2 !== null && cocktail.strIngredient2 !== "" && cocktail.strIngredient2 !== ''){
                array.push(cocktail.strIngredient2)
            }
           if(cocktail.strIngredient3 !== null && cocktail.strIngredient3 !== "" && cocktail.strIngredient3 !== ''){
                array.push(cocktail.strIngredient3)
            }

            return array;
        },
        getMessurements(){

        }
    }
}
</script>

<style scoped>
    h1 {
        text-decoration: underline white;
        text-align: center;
    }
</style>