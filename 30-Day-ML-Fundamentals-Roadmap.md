# 30-Day Machine Learning Fundamentals Roadmap

**Context used:**
- Situation: BTech CSE student (AI specialization)
- Current skills: Python, data analysis basics, prompt engineering (just completed)
- Goal: ML fundamentals — Phase 2 of your 6-month AI Engineer roadmap
- Time: ~1–1.5 hrs/day
- Level: Beginner in ML (not in Python)
- Style: Project-first, portfolio-oriented

**Goal:** Understand core ML concepts deeply enough to build, evaluate, and explain real models — ending with a portfolio project on GitHub.

---

## Week 1 (Days 1–7): Math Intuition + Data Handling

**Milestone:** Comfortable manipulating data and understanding the math behind ML without getting stuck in theory.

| Day | Task | Resource |
|---|---|---|
| 1 | Review NumPy essentials: arrays, broadcasting, vectorized ops | NumPy official quickstart |
| 2 | Pandas deep-dive: groupby, merge, handling missing data | Kaggle "Pandas" micro-course |
| 3 | Statistics refresher: mean/median/variance, distributions, correlation | StatQuest (YouTube) — "Statistics Fundamentals" playlist |
| 4 | Linear algebra intuition: vectors, dot product, matrix multiplication (visual, not proof-heavy) | 3Blue1Brown — "Essence of Linear Algebra" (first 3 videos) |
| 5 | Data visualization: matplotlib/seaborn for EDA | Kaggle "Data Visualization" course |
| 6 | Practice: full EDA (exploratory data analysis) on one public dataset (e.g. Titanic) | Kaggle Titanic dataset |
| 7 | **Mini-project:** Publish a clean EDA notebook (charts + insights) on GitHub | — |

---

## Week 2 (Days 8–14): Supervised Learning — Regression & Classification

**Milestone:** Train, and explain, your first regression and classification models.

| Day | Task | Resource |
|---|---|---|
| 8 | Learn linear regression: intuition, cost function, gradient descent (conceptual) | StatQuest — "Linear Regression" |
| 9 | Implement linear regression with scikit-learn on a simple dataset | scikit-learn docs — Linear Models |
| 10 | Learn logistic regression for classification | StatQuest — "Logistic Regression" |
| 11 | Implement logistic regression; understand decision boundaries | scikit-learn docs |
| 12 | Learn decision trees & random forests (intuition + when to use) | StatQuest — "Decision Trees" / "Random Forest" |
| 13 | Implement a random forest classifier; compare accuracy vs logistic regression | scikit-learn docs |
| 14 | **Mini-project:** Build a classifier on a new dataset (e.g. loan approval or heart disease) — compare 2 models | Kaggle datasets |

---

## Week 3 (Days 15–21): Model Evaluation, Feature Engineering, Unsupervised Learning

**Milestone:** Move beyond "does it run" to "is it actually good" — evaluate models properly and explore unlabeled data.

| Day | Task | Resource |
|---|---|---|
| 15 | Learn train/test split, cross-validation, overfitting vs underfitting | StatQuest — "Cross Validation" |
| 16 | Learn evaluation metrics: accuracy, precision, recall, F1, confusion matrix | StatQuest — "Confusion Matrix" |
| 17 | Learn ROC/AUC for classification evaluation | StatQuest — "ROC and AUC" |
| 18 | Feature engineering basics: encoding categoricals, scaling, handling outliers | scikit-learn preprocessing docs |
| 19 | Learn unsupervised learning: k-means clustering (intuition + implementation) | StatQuest — "K-means clustering" |
| 20 | Learn dimensionality reduction: PCA (conceptual + basic implementation) | StatQuest — "PCA" |
| 21 | **Mini-project:** Re-do Week 2's classifier with proper cross-validation, tuned features, and full metric reporting | — |

---

## Week 4 (Days 22–30): Capstone Project + Portfolio + Publishing

**Milestone:** Ship one complete, well-evaluated ML project with public documentation.

| Day | Task | Resource |
|---|---|---|
| 22 | Pick a capstone dataset/problem (ideally public-welfare angle, matching your interests) | Kaggle / UCI ML Repository |
| 23 | Full EDA + define the problem clearly (regression vs classification, success metric) | — |
| 24 | Feature engineering + baseline model | — |
| 25 | Try 2–3 model types, compare with cross-validation | scikit-learn docs |
| 26 | Tune the best model (GridSearchCV or simple manual tuning) | scikit-learn — Model Selection |
| 27 | Write clear evaluation summary — which model won, why, trade-offs | — |
| 28 | Write README: problem, approach, results, what you'd improve next | GitHub |
| 29 | Push full project to GitHub with clean notebook + README | GitHub |
| 30 | **Capstone Review:** Turn the project into a LinkedIn post — the story of one dataset, one problem, one decision-making process | ABTalks format |

---

## Final Outcome (Day 30)

By the end of 30 days, you'll have:
- Solid working knowledge of **regression, classification, evaluation, and basic unsupervised learning**
- A complete **ML capstone project on GitHub** — EDA, modeling, evaluation, README
- A **LinkedIn post** documenting your ML learning journey (continuing your visibility-building habit)
- A clear bridge into **Phase 3: Deep Learning** on your 6-month AI Engineer roadmap

**Natural next step:** Use this capstone as your reference project when starting Deep Learning — you'll revisit the same dataset-to-deployment mindset with neural networks.
