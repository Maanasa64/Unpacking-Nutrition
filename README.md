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

Examining the relationship between calorie counts and user ratings is not only pertinent to understanding taste preferences and nutritional values but also holds significant implications for health and well-being. In today's society, where concerns about obesity, diabetes, and other diet-related health issues are prevalent, understanding how nutritional content influences user satisfaction becomes crucial.

Calorie count is a fundamental aspect of nutritional information, directly tied to energy intake and expenditure. Foods with higher calorie counts often contain higher levels of fat, sugar, and carbohydrates, which, if consumed excessively, can contribute to weight gain and other health problems. On the other hand, foods with lower calorie counts may be perceived as healthier options, promoting satiety without excessive energy intake.

User ratings provide valuable insights into consumer preferences and perceptions of food products. By analyzing how user ratings correlate with calorie counts, we can gain a deeper understanding of how individuals perceive the relationship between taste, satisfaction, and nutritional content. This understanding can inform dietary recommendations, food labeling policies, and interventions aimed at promoting healthier eating habits.


## Data Cleaning and Exploratory Data Analysis

To clean the data appropriately, we will perform the following steps:

1. Replace missing or inappropriate values with NaN where necessary.
   This step ensures that our data is consistent and suitable for analysis. In the provided code, missing ratings (denoted as 0) are replaced with NaN using the replace() function from the NumPy library (np.nan). This ensures that any missing or inappropriate values in the 'rating' column are appropriately handled and do not affect subsequent analyses.

3. Convert relevant columns to appropriate data types.
   It's essential to use the correct data types for each column to perform meaningful analyses. In the provided code, columns containing date information (`submitted` and `date`) are converted to datetime objects using the `pd.to_datetime()` function. This conversion allows us to perform date-based operations and analyses accurately.

5. Extract useful information from columns such as dates or text.
   Sometimes, valuable insights can be derived by extracting useful information from existing columns. In the provided code, the `submitted` and `date` columns are split into separate columns for year, month, and day using datetime properties (`dt.year`, `dt.month`, `dt.day`). This allows us to analyze trends over time more effectively and explore variations in interactions and submissions across different time periods.



