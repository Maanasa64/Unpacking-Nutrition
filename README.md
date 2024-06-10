# Unpacking-Nutrition: The Relationship Between Foods with High Calorie Count and their Ratings

Authors: Maanasa Prasad & Ria Juneja

## Introduction

Welcome to our exploration of nutritional content in food products over time. In this analysis, we delve into a rich dataset encompassing various culinary creations, from ingredients and preparation methods to nutritional profiles and user ratings.

Our dataset provides a comprehensive view of food products, including details such as ingredients, number of steps and ingredients, nutritional values, and user ratings. This diverse range of information opens up numerous avenues for analysis and exploration.

### Questions of Interest:

1. Do dishes with higher calorie counts tend to receive higher ratings from users?

2. How have the nutritional profiles of food products changed over time?

3. Are there any correlations between specific ingredients and user ratings?

### Question of Focus:

Among these questions, we choose to investigate the following question further:

Do dishes with higher calorie counts tend to receive higher ratings from users?

This inquiry delves into the intersection of taste preferences, nutritional values, and user perceptions, setting the stage for an insightful exploration into the world of food and nutrition. By examining the relationship between calorie counts and user ratings, we aim to understand how nutritional content influences user satisfaction and preferences in the culinary domain.

### More about the datasets

We use 2 datasets in our investigation:

1. `recipe` has `83782 rows × 12 columns`:
The first dataset, `recipe`, contains 83782 rows, indicating 83782 unique recipes, with 10 columns recording the following information:

| Column             | Description                                                                                                                                                                                       |
| :----------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `'name'`           | Recipe name                                                                                                                                                                                       |
| `'id'`             | Recipe ID                                                                                                                                                                                         |
| `'minutes'`        | Minutes to prepare recipe                                                                                                                                                                         |
| `'contributor_id'` | User ID who submitted this recipe                                                                                                                                                                 |
| `'submitted'`      | Date recipe was submitted                                                                                                                                                                         |
| `'tags'`           | Food.com tags for recipe                                                                                                                                                                          |
| `'nutrition'`      | Nutrition information in the form [calories (#), total fat (PDV), sugar (PDV), sodium (PDV), protein (PDV), saturated fat (PDV), carbohydrates (PDV)]; PDV stands for “percentage of daily value” |
| `'n_steps'`        | Number of steps in recipe                                                                                                                                                                         |
| `'steps'`          | Text for recipe steps, in order                                                                                                                                                                   |
| `'description'`    | User-provided description                                                                                                                                                                         |
| `'ingredients'`    | Text for recipe ingredients                                                                                                                                                                       |
| `'n_ingredients'`  | Number of ingredients in recipe                                                                                                                                                                   |

2. `interaction` has `731927 rows × 5 columns`

| Column        | Description         |
| :------------ | :------------------ |
| `'user_id'`   | User ID             |
| `'recipe_id'` | Recipe ID           |
| `'date'`      | Date of interaction |
| `'rating'`    | Rating given        |
| `'review'`    | Review text         |

