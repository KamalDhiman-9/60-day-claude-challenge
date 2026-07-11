# NutriScope — v1 → v2 Changelog

A single-file, no-backend nutrition tracker built with vanilla JS + Chart.js. This document compares the initial MVP against the enhanced release.

## Summary

| | v1 (MVP) | v2 (Enhanced) |
|---|---|---|
| Tabs | 4 | 7 |
| Foods in database | 20 | 60 |
| Tracked nutrients | 10 | 16 |
| Charts | 1 | 4 |
| Log entry fields | food, qty, unit | food, qty, unit, **day, meal** |

---

## 🆕 New Features

### CSV Upload
Bulk-import a food log via CSV (`food, quantity, unit, day, meal`). Includes a downloadable template and per-row validation errors for unrecognized foods or units.

### 2-Day Meal Planner
Log entries now carry a `day` (1/2) and `meal` (Breakfast/Lunch/Dinner/Snack). A dedicated Meal Planner tab breaks both days out by slot with subtotals, plus a Day 1 vs Day 2 comparison chart.

### Risk Analysis
Severity-ranked (Low / Moderate / High) flags for chronic nutrient patterns — e.g. low iron, low B12, high sodium, chronic calorie deficit/surplus. Framed as educational pattern-flags, not a diagnosis.

### Educational Disclaimer
Persistent banner across the app, plus a full disclaimer section in the new Sources tab, clarifying this is not medical advice.

### Nutrition Sources
New tab citing USDA FoodData Central and Indian Food Composition Tables (IFCT 2017, NIN/ICMR) for food values, and ICMR-NIN guidelines for RDA targets.

### Day / Scope Selector
Dashboard, Risk Analysis, and Recommendations now share a **Day 1 / Day 2 / 2-Day Average** selector to view any metric per-day or averaged.

---

## 📈 Expanded Features

### Food Database: 20 → 60
40 new foods added: atta, besan, bajra, jowar, sooji, poori, paratha, upma, sambar, rasam, buttermilk, ghee, butter, cheese, soy chunks, tofu, peanuts, almonds, cashew, walnuts, sesame seeds, flaxseeds, pumpkin seeds, sunflower seeds, mango, papaya, orange, guava, pomegranate, grapes, watermelon, tomato, onion, carrot, cabbage, cauliflower, beetroot, cucumber, sweet potato, green peas.

### Tracked Nutrients: 10 → 16
Added Sodium, Potassium, Magnesium, Zinc, Vitamin A, Folate. Sodium is treated as an **upper limit** rather than a target — it's only flagged when intake exceeds 100%, not when it's low.

### Micronutrient Rings: 6 → 12
Ring cluster now covers fiber, iron, calcium, vitamin C, vitamin D, B12, sodium, potassium, magnesium, zinc, vitamin A, and folate.

### Charts: 1 → 4
- Macro grams bar chart (consumed vs target) — *carried over from v1*
- **Calorie-source doughnut** (% calories from protein/carbs/fat)
- **Micronutrient radar chart** (shape of intake across all 12 micronutrients)
- **Day 1 vs Day 2 comparison bar chart** (Meal Planner tab)

### Recommendations Engine
- Smart Swaps now work bidirectionally — suggests lighter alternatives for excesses, not just stronger alternatives for deficiencies
- New **Personalized Insights** section: diet-aware tips (e.g. pairing iron with vitamin C for absorption, B12 sourcing for vegetarians/eggetarians, sodium/fiber pattern callouts)

---

## ➖ Unchanged
- Profile inputs and BMR/TDEE/macro target formulas (Mifflin-St Jeor based)
- Dark premium visual theme and card-based layout
- Add / edit / remove workflow for food log entries
- Single-file, no-backend, localStorage-persisted architecture
