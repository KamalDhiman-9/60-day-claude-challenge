# Day 17 — Fuel Cost Intelligence Dashboard (E85 Paradox Analysis)

## 🎯 Objective
Analyze a multi-fuel vehicle cost dataset (Petrol, E85 Flex-Fuel, Diesel, CNG, EV) and build an interactive HTML dashboard to compare cost/km, CO₂ emissions, maintenance, and refuel time — with a focus on the counter-intuitive **E85 "paradox"**: cheaper pump price but not always cheaper to run.

**Vehicle profile used for personalization:** TVS Jupiter 125 (2025), Petrol, City usage, 500 km/month, Age 1 year.

---

## 🛠️ What I Did

1. Reviewed KPI cards, fuel comparisons, maintenance costs, and environmental impact analysis.
2. Analyzed E85 economics and break-even calculations.
3. Reviewed SVG charts, gauges, and fuel comparisons.
4. Saved the generated HTML dashboard file.
5. Opened the dashboard in the browser.
6. Took screenshots of the dashboard.
7. Created a `Day17` folder in the GitHub repository.
8. Created a `day17.md` file (this file).
9. Uploaded screenshots, the generated HTML, analysis findings, and learnings.
10. Committed and pushed the changes.

---

## 📊 Key Insights from the Dataset (52 records)

| Fuel | Cost/km | CO₂/km | Maintenance/km | Refuel Time |
|---|---|---|---|---|
| Electric (EV) | ₹1.75 | 0.091 kg | ₹0.23 | 45 min |
| CNG | ₹3.32 | 0.125 kg | ₹0.66 | 8 min |
| Diesel | ₹4.67 | 0.179 kg | ₹1.00 | 5 min |
| Petrol (E20) | ₹6.15 | 0.171 kg | ₹0.47 | 5 min |
| E85 (Flex-Fuel) | ₹6.37 | **0.070 kg (lowest)** | ₹0.46 | 5 min |

### ⚡ The E85 Paradox
- **Pump price saving vs Petrol:** ~18% cheaper per litre (₹82 vs ₹100).
- **Running cost penalty:** despite the cheaper pump price, E85's lower mileage (12.87 km/l vs 16.27 km/l) makes it ~**3.6% more expensive per km** to actually run than plain Petrol.
- **Break-even price:** E85 would need to be priced at or below **₹79.10/L** to match Petrol's running cost — its real-world price of ₹82/L sits just above that line.
- **Where E85 wins:** it has the **lowest CO₂ emissions per km of any fuel in the dataset**, beating even EV and CNG.

### 🧮 E85 Score: 6.6 / 10
Scoring weights — Cost (4pt), CO₂ (3pt), Refuel time (2pt), Maintenance (1pt):
- CO₂: full marks (best-in-class emissions)
- Refuel time: full marks (matches petrol/diesel at 5 min)
- Cost/km: low score (highest running cost among liquid fuels)
- Maintenance: mid score (close to petrol, well above EV)

**Verdict:** E85 is the clear environmental winner but a mild economic trade-off — a good pick for emission-conscious riders willing to absorb a small running-cost premium, not a pure cost-saver.

### 📈 Age Impact
- Cost/km rises with vehicle age across every fuel type — Diesel shows the steepest climb (₹4.35/km new → ₹5.29/km at 10+ years), largely driven by rising maintenance costs.
- For a 1-year-old vehicle (like the reference TVS Jupiter), all fuels sit near their lowest lifetime cost/km — the "New (0–2y)" bucket is the cheapest window across the board.

---

## 📁 Files in this folder
- `e85_dashboard.html` — full interactive dashboard (SVG bar chart, donut chart, age-trend line chart, animated gauge, fuel comparison cards)
- Dashboard screenshots (KPI cards, charts, gauge, fuel cards)

---

## 🧠 Learnings
- Pump price alone is a misleading fuel-economy signal — mileage (efficiency) matters just as much as price/litre; E85's cheaper price is largely offset by lower energy density/mileage.
- Emissions and running cost don't always align — E85 is the greenest option here but not the cheapest, a useful reminder that "eco" and "economical" are different axes.
- Grouping cost data by vehicle-age buckets surfaces maintenance trends that a single aggregate average would hide.
- Building all charts in hand-coded SVG (no chart libraries) keeps the dashboard fully offline and dependency-free, and forces a clearer understanding of how bar/donut/line/gauge geometry actually works.

---

**GitHub commit URL:** _add your commit link here after pushing_
`https://github.com/<your-username>/<your-repo>/commit/<commit-hash>`
