---
layout: post
title: Learn 🤔
search_exclude: true
permalink: /create_and_compete/zoominguess
menu: nav/create_and_compete.html
author: Mirabelle, Arshia, Prajna, Claire, Zoe, Sanya
---


<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>African Recipes Finder</title>
 <style>
    body {
        font-family: Arial, sans-serif;
        background-color: #a69c6c;
        color: #96a66c;
        margin: 20px;
    }
    h1 {
        color: #2c3e50;
    }
    .container {
        max-width: 600px;
        margin: 0 auto;
        background-color: #a69c6c;
        padding: 20px;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    select, button {
        width: 100%;
        padding: 10px;
        margin: 10px 0;
        font-size: 16px;
        border: 1px solid #ccc;
        border-radius: 4px;
    }
    .recipe-output {
        margin-top: 20px;
        padding: 20px;
        background-color: #96a66c;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
</style>
<body>
    <h1 style="
    color: #d2b48c; /* Light brown (Tan) */
    font-family: 'Comic Sans MS', 'Brush Script MT', cursive; /* Fun and playful font */
    font-size: 3.5em; /* Adjusted size for emphasis */
">African Recipes Finder</h1>
    <div class="container">
        <form id="recipeForm">
            <label for="country">Choose a Country in Africa:</label>
            <select id="country">
                <option value="Nigeria">Nigeria</option>
                <option value="South Africa">South Africa</option>
                <option value="Ethiopia">Ethiopia</option>
                <option value="Kenya">Kenya</option>
                <option value="Ghana">Ghana</option>
            </select>
            <label for="type">Sweet or Savory?</label>
            <select id="type">
                <option value="sweet">Sweet</option>
                <option value="savory">Savory</option>
            </select>
            <button type="button" onclick="getRecipe()">Get Random Recipe</button>
        </form>
        <div id="recipeOutput" class="recipe-output">
            <!-- Recipe output will be displayed here -->
        </div>
    </div>
    <script>
        const recipes = {
            "Nigeria": {
                "sweet": [
                    "Chin Chin - Fried dough snack.",
                    "Nigerian Coconut Rice Pudding."
                ],
                "savory": [
                    "Jollof Rice - A popular rice dish.",
                    "Egusi Soup - Melon seed soup with meat."
                ]
            },
            "South Africa": {
                "sweet": [
                    "Malva Pudding - A traditional dessert.",
                    "Milk Tart - A South African custard tart."
                ],
                "savory": [
                    "Bobotie - A spiced minced meat dish.",
                    "Bunny Chow - Curry in a hollowed-out loaf of bread."
                ]
            },
            "Ethiopia": {
                "sweet": [
                    "Baklava - A sweet pastry with nuts and syrup.",
                    "Dabo Kolo - Sweet and spicy fried dough balls."
                ],
                "savory": [
                    "Doro Wat - Spicy chicken stew.",
                    "Kitfo - Minced raw beef with spices."
                ]
            },
            "Kenya": {
                "sweet": [
                    "Mandazi - Fried dough pastry.",
                    "Kenyan Coconut Cake."
                ],
                "savory": [
                    "Ugali - Maize meal served with stew.",
                    "Nyama Choma - Grilled meat."
                ]
            },
            "Ghana": {
                "sweet": [
                    "Chibom - Sweet bread rolls.",
                    "Ghanaian Rice Balls with Groundnut Soup."
                ],
                "savory": [
                    "Fufu and Light Soup - A staple dish.",
                    "Ghanaian Jollof Rice."
                ]
            }
        };
        function getRecipe() {
            const country = document.getElementById("country").value;
            const type = document.getElementById("type").value;
            // Fetch a random recipe from the selected country and type (sweet/savory)
            const countryRecipes = recipes[country][type];
            const randomRecipe = countryRecipes[Math.floor(Math.random() * countryRecipes.length)];
            // Display the recipe
            const output = document.getElementById("recipeOutput");
            output.innerHTML = `<h3>Random Recipe from ${country} (${type}):</h3><p>${randomRecipe}</p>`;
        }
    </script>

</body>

**NEED TO CONNECT TO AN API DATABASE OF AFRICAN RECIPIES

