# Cado

**Released iOS app · Source code private**

[View on the App Store](https://apps.apple.com/us/app/cado-meal-prep-coach/id6797121303) · [Tributary Studios](https://tributarystudios.com/)

Cado turns food preferences, schedules, and serving needs into weekly meal plans, recipes, and a combined grocery list. It serves people who want to plan their meals and shopping together, including those cooking for one or deliberately preparing extra portions.

## My contribution

I developed Cado through Tributary Studios, including its SwiftUI interfaces, local SwiftData models, meal-plan and grocery workflows, and the integration with a server-side generation proxy. The public App Store listing identifies Tributary Studios LLC as the developer and seller.

## Workflow

![Three actual Cado simulator views: a planned day with meals, a grocery checklist grouped by category, and a recipe with ingredients and cooking steps.](../assets/cado/workflow.png)

1. **Review the plan.** Browse scheduled meals and open a recipe from the selected day.
2. **Shop the list.** Track purchased items in a categorized list connected to the week's meals.
3. **Cook the meal.** Read serving quantities, ingredients, and instructions in the recipe detail.

Full-size views: [plan](../assets/cado/01-plan.png) · [groceries](../assets/cado/02-groceries.png) · [recipe](../assets/cado/03-recipe.png).

These are existing, authentic simulator captures from the documented v1.0.2 marketing-fixture set. The displayed nutrition, prices, and purchase counts are demonstration values. Interface content has not been generated or replaced for this portfolio; these are independent copies of the raw captures.

## Engineering decision

Generated text needs to become consistent application data. The plan-generation pipeline checks the expected meal slots, content, and applicable nutrition constraints before accepting a plan for storage. This introduces validation and retry complexity, but gives the app a defined way to reject malformed output instead of persisting every response. Local SwiftData models then connect meals, recipes, and grocery records across the app.

**Technology:** Swift, SwiftUI, SwiftData, StoreKit, and a TypeScript proxy on Firebase Cloud Functions for generation requests. Plans persist locally; generation requests are processed through the backend.

## Status and evidence

Cado has a public App Store listing with a **v1.0.2** version-history entry dated August 22, 2026. The screenshots demonstrate the implemented plan-to-shopping-to-recipe workflow. They are fixture captures, not a benchmark of plan generation or evidence of health outcomes. Ongoing development changes are not presented as verified App Store behavior.

Cado provides general meal-planning and nutrition information, not medical advice. Source code remains private.

[Back to profile](../README.md)
