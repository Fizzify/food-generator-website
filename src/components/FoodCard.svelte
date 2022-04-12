<script>
  export let food;

  if (food.strTags === null) {
    food.strTags = "No tags for this one. :(";
  }
</script>

<h2>Food Generator</h2>
<p>Made by Fizzify</p>
<div class="food-card">
  <h1 class="food-title">{food.strMeal}</h1>
  <p class="food-tags">Tags: {food.strTags}</p>
  <p><a href="{food.strYoutube}" target="__blank"><em>{food.strYoutube}</em></a></p>
  <img class="food-img" src="{food.strMealThumb}" alt="Food image" />
  <p>Category: {food.strCategory}</p>
</div>
<div class="btn"><a class="generate" href="https://darling-croissant-57c887.netlify.app/">Generate</a></div>
