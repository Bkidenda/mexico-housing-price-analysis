# 🏠 Mexico Housing Price Analysis

**Does property size or location drive real estate prices in Mexico?**
An exploratory data analysis uncovering a Simpson's Paradox in a 1,736-property dataset spanning 29 Mexican states.

## 📌 Research Question

Are property prices in Mexico more influenced by property size or by location?

## 🔍 Key Findings

- **National correlation between size and price is moderate (r ≈ 0.59)** — but this single number hides enormous state-level variation, from r ≈ 0.0 to r ≈ 0.9+. This is a textbook case of **Simpson's Paradox**: an aggregate statistic disguising contradictory subgroup behavior.
- **Location drives real, substantial differences in price per square meter.** The median price/m² in Distrito Federal ($958.89) is nearly **3x** Colima's ($334.17).
- **But location alone explains only ~12% of total price-per-m² variation nationally** — size and other within-state factors account for the majority of the variation.
- **Controlling for size cut "unexplained" within-state variance nearly in half** (78.3% → 38.5%), showing that a large share of what looked like noise was actually size differences in disguise.

**Bottom line:** neither size nor location dominates outright. Location sets a meaningful floor/ceiling on price per m², but most of the actual variation happens *within* a given state — and a good chunk of that is size, not randomness. The honest answer is: both matter, and pretending one factor "wins" oversimplifies what the data shows.

## 📊 Project Structure
notebooks/
├── 01_data_cleaning.ipynb # Merging 3 raw CSVs, fixing currency strings, parsing lat-lon
├── 02_visualizing_housing_data.ipynb # Distributions, outlier handling, scatterplots
├── 03_correlations_and_variable_relationships.ipynb # National vs. state-level correlation, Simpson's Paradox
└── 04_grouped_analysis_price_per_m2.ipynb # Price-per-m², variance decomposition by state


## 🛠️ Tools Used

Python · pandas · matplotlib · seaborn · numpy · Jupyter Notebook

## ▶️ How to Run

```bash
git clone https://github.com/Bkidenda/mexico-housing-price-analysis.git
cd mexico-housing-price-analysis
pip install -r requirements.txt
jupyter notebook
```

Run the notebooks in order (01 → 04); each one builds on the cleaned dataset produced by the previous step.

## 👤 Author

**Brian Kidenda**
[LinkedIn](https://linkedin.com/in/bkidenda) · bkidenda@gmail.com
