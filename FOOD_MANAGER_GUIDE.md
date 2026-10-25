# Tubby Family Food Manager Guide

## Stock filters
Use **All**, **Fridge**, **Freezer**, or **Pantry** to filter the shared food stock. **Needs checking** shows items missing important details or whose dates need attention. Select **Edit** on an item to fill in highlighted details.

## Meal suggestions
Open **Meals** to load up to five meal ideas. Turn **Prioritise food near its date** on to ask the AI to use items approaching their use-by or best-before date first. Near-date ingredients are flagged when identified by the AI. Ingredient names are **green** when linked to current stock and **red** when missing or not confirmed. Tap **Recipe** to reveal cooking instructions. **Add missing to shopping** adds missing ingredients to the shared list. **Cooked it — update stock** opens the stock deduction flow for ingredients used.

## Shared shopping list
Type one item or a comma-separated list such as `bread, eggs, baked beans`, then tap **Add & organise with AI**. The AI splits typed items, standardises names, and groups items into supermarket sections. It also organises unchecked items already on the shared list. The family shares the list across signed-in devices.

Tick items as you shop. Tap **Finish shop & archive ticked items** to archive checked items; unchecked items stay on the active list.

## Notes
AI suggestions and list organisation require the family Gemini API key to be configured in Admin Settings. Check AI-generated item names, quantities, and date details before relying on them.

## Diet scans and nutrition memory
When logging food, review AI nutrition estimates and correct them against the package label where possible. If you manually edit any nutrient value and save the entry, Tubby saves the corrected values in the family's nutrition memory. Future scans load those saved corrections before asking AI, so matching products can reuse the family's values. Nutrition memory is shared across family members. A clear product name/brand in the title or notes helps future matching. The avocado icon in the top-left returns to the main home screen.

The diet entry form now measures **fibre (g)** and **salt (g)** as well as calories, protein, carbohydrates and fat. Today's fibre and salt totals appear on the dashboard. For packaged foods, use the label's per-serving values and double-check the serving size, particularly when logging food for children.

**Deployment note:** nutrition memory requires the `nutritionMemory` Firestore rule in `firestore.rules` as well as the updated `Public/index.html`. Deploy both to Firebase for cross-device memory to work.
