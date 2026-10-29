# Cado

**Available on the App Store · Source code private**

[App Store](https://apps.apple.com/us/app/cado-meal-prep-coach/id6797121303) · [Tributary Studios](https://tributarystudios.com/)

iOS application for weekly meal planning, recipes, and grocery lists. Plans account for food preferences, schedules, and the number of people eating.

## Contributions

- Developed the application through Tributary Studios, including SwiftUI interfaces and local SwiftData models.
- Built meal-plan, recipe, and grocery-list functions and integrated the server-side generation proxy.
- Implemented validation of generated meal plans before storing them in the application.

## Screenshots

![Cado screens showing a planned day, a categorized grocery checklist, and recipe ingredients and instructions.](../assets/cado/workflow.png)

1. **Meal plan:** Review scheduled meals and open recipes.
2. **Grocery list:** Track purchases by category.
3. **Recipe:** Review servings, ingredients, and cooking instructions.

Full-size screenshots: [meal plan](../assets/cado/01-plan.png) · [grocery list](../assets/cado/02-groceries.png) · [recipe](../assets/cado/03-recipe.png).

Screenshots are from the v1.0.2 simulator capture set and use sample data. Nutrition values, prices, and purchase counts are demonstration values.

## Design decision

Generated plans are checked for required meal slots, content, and applicable nutrition constraints before storage. Validation and retries add complexity, but allow invalid responses to be rejected before storage. SwiftData stores the accepted meals, recipes, and grocery records locally; generation requests are processed through the backend.

**Technologies:** Swift, SwiftUI, SwiftData, StoreKit, TypeScript, Firebase Cloud Functions.

## Status

Version v1.0.2 is listed on the [App Store](https://apps.apple.com/us/app/cado-meal-prep-coach/id6797121303), dated August 22, 2026. The public release and ongoing development changes are tracked separately. Source code is private.

Cado provides general meal-planning and nutrition information, not medical advice.

[Back to profile](../README.md)
