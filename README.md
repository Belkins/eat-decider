# Eat Decider

**Eat Decider** is a single-page HTML tool that helps users decide what to eat for dinner based on their dietary restrictions, hunger level, food cravings, budget, and cooking effort. It offers meal recommendations—from delivery options to quick & easy recipes to chef-mode cooking—along with detailed instructions and a handy shopping list generator.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [How It Works](#how-it-works)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

- **Purpose:** Quickly narrow down dinner choices by filtering through dietary preferences, hunger level, craving type, budget, and cooking effort.
- **Technology Stack:** 
  - **HTML** for structure
  - **Tailwind CSS** for styling
  - **JavaScript** for interactivity

Everything is contained in a single HTML file, making it straightforward to open in a browser and use immediately.

---

## Features

1. **Dietary Restrictions Selection**  
   - Choose among vegetarian, vegan, gluten-free, dairy-free, or none.

2. **Hunger Level**  
   - Starving, quite hungry, or just peckish.

3. **Craving Type**  
   - Savory, spicy, fresh, or comfort food.

4. **Budget**  
   - Low ($), medium ($$), or high ($$$).

5. **Effort Level**  
   - Delivery (no cooking), quick & easy, or chef mode.

6. **Recipe Details**  
   - Recipes come with:
     - Prep time
     - Cook time
     - Ingredients
     - Step-by-step instructions
     - Optional cooking tips

7. **Shopping List Generator**  
   - Check off the ingredients you need for your selected recipe.

8. **Progress Bar**  
   - A handy progress bar at the top to show which step you’re on.

9. **Start Over**  
   - A simple reset button to begin a new decision-making process at any time.

---

## How It Works

1. **User Selections**  
   As users answer each question (diet, hunger, craving, etc.), the script updates the `preferences` object in the background.

2. **Filtering**  
   The script filters through three arrays of meal options:
   - `deliveryOptions`
   - `quickAndEasyOptions`
   - `chefModeOptions`

   Based on the user’s final preferences, one best match is returned (or a fallback if no perfect match is found).

3. **Recipe Display**  
   - If the chosen suggestion has a `recipeKey`, the detailed recipe is displayed along with a "Generate Shopping List" button.
   - The shopping list section shows all ingredients as a checklist for easy reference.

4. **Reset**  
   - Clicking **Start Over** clears all preferences and resets the quiz to the first step.

---

## Getting Started

1. **Download or Clone** this repository containing the `index.html` (the single-page file).
2. **Open the file** in a web browser (e.g., Chrome, Firefox, Safari).

No additional setup is required since external dependencies are loaded via CDNs.

---

## Usage

1. **Open** the `index.html` file in your browser.  
2. **Answer each question** in order:
   - Select dietary restrictions (you can choose multiple or “No Restrictions”).
   - Click **Confirm & Continue**.
   - Choose hunger level, craving, budget, and effort.
3. **Get your suggestion**:
   - If **Delivery** is chosen, you’ll see a recommended delivery option.
   - If **Quick & Easy** or **Chef Mode** is chosen, you may also get a recipe with the option to view details.
4. **(Optional) Generate Shopping List**:
   - If a recipe is shown, click **Generate Shopping List** to display the required ingredients in a checklist.
5. **Start Over** at any time by clicking **Start Over** to clear your selections and begin again.

---

## Customization

- **Tailwind Version**: This file uses the Tailwind CSS CDN (`https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css`). You can update the URL for a newer Tailwind version or replace it with a local version of Tailwind if desired.
- **Meal Options**: The arrays `deliveryOptions`, `quickAndEasyOptions`, and `chefModeOptions` (along with the `recipes` object) can be edited to add, remove, or modify your meal recommendations.
- **Styling**: Tailwind classes can be changed directly in the HTML to adjust colors, spacing, and layout.
- **Recipe Data**: The `recipes` object contains all recipe details. Adding a new recipe requires:
  - A unique `recipeKey`
  - A corresponding JSON-like entry (name, prepTime, cookTime, ingredients, instructions, tips, etc.)

---

## Contributing

Contributions are welcome! Here’s how you can help:

1. **Fork** this repository.  
2. **Create a new branch** (e.g., `feature/new-delivery-options`).
3. **Commit changes** (e.g., update meal arrays or enhance UI/UX).
4. **Open a Pull Request** detailing your changes and why they should be merged.

---

## License

This project is provided under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and distribute this code as you see fit. 

Enjoy your perfect meal with **Eat Decider**! Bon appétit!
