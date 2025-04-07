# 🔮 autosage: The Fantasy Data Science Library

> *"One spell to cleanse your data, many charms to reveal its secrets."*

**autosage** is a minimalist and intelligent data science library that grants data scientists the power to handle complex preprocessing and feature engineering with a single incantation. Designed to be the *ultimate preprocessing spellbook*, it seamlessly prepares your dataset for machine learning — so you can focus on the magic of insights, not the monotony of cleanup.

---

## 🧙‍♂️ The Vision

In every data scientist’s journey, there lies a forest of missing values, cursed encodings, shapeshifting scales, and mysterious features waiting to be revealed. **autosage** is your enchanted guide through that forest.

- 🧠 **Minimal API, Maximum Intelligence**
- ❤️ **Smart Defaults for Common Problems**
- 🛠️ **Built From Scratch for True Flexibility**
- 🧬 **All-in-One Preprocessing Spell**
- ✨ **Feature Engineering Without The Pain**
- 🔍 **Data Visualization in its Purest Form**
- 🤖 **AI-Driven Insight Wizardry**

---

## 🧝 Module Spellbook

```
autosage/
│
├── core/             # Data type analysis, summaries, smart detectors
├── preprocess/       # Missing values, encoding, scaling
├── features/         # Date/text-based features, interactions, importance
├── visuals/          # Lightweight EDA visuals
├── advisor/          # AI-powered module for next-step suggestions
├── viewer/           # Beautiful tabular display for all datasets, including JSONs
├── magic/            # Orchestrates all internal transformations
└── Sage.py           # The single-command spellcaster
```

---

## 🧞 Sage: The One-Command Wizard

```python
from autosage import Sage

clean_df = Sage().fit_transform(df, target='SalePrice')
```

### Spell Configuration

| Spell Component       | Default    | Description |
|------------------------|------------|-------------|
| `handle_missing`       | `'smart'`  | Smart imputation for numerical and categorical values |
| `encode`               | `'auto'`   | Automatically chooses encoding based on cardinality |
| `scale`                | `'zscore'` | Standardization method (zscore, minmax, robust, etc.) |
| `generate_features`    | `True`     | Extracts datetime, text, and interaction features |
| `log_steps`            | `True`     | Logs every transformation step performed |
| `verbose`              | `False`    | Prints magical reasoning behind transformations |

---

## 🧙‍♀️ What `fit_transform()` Does

> **All in one enchanted gesture:**

1. 🧹 **Initial Cleanup**
   - Detects column types and structure
   - Drops high-missing or irrelevant columns

2. ✨ **Missing Value Handling**
   - Numerical: mean/median/knn
   - Categorical: mode/“Unknown”/predictive

3. 🎯 **Encoding**
   - Low cardinality → One-Hot  
   - Medium cardinality → Frequency / Ordinal  
   - High cardinality → Smart leave-as-is or hash

4. 🧪 **Scaling**
   - Z-score, Min-Max, or Robust based on distribution

5. 🧬 **Feature Generation**
   - Extracts datetime parts: year, month, weekday, etc.  
   - Text features: word count, length, sentiment scores (coming soon)  
   - Feature interaction terms (optional)

6. 🧠 **Feature Selection**
   - Low variance filter  
   - Correlation pruning  
   - Mutual information with target (if provided)

7. 📊 **Tabular Visualization (even for JSON!)**
   - Data is displayed beautifully in tables—even nested JSONs are transformed into readable tabular formats with expandable insights.

8. 🤖 **AI Advisor: The Sage’s Counsel**
   - Post-preprocessing, the built-in AI reviews your dataset and suggests:
     - Suitable ML algorithms
     - Next preprocessing or modeling steps
     - Feature importance observations
     - Potential data issues still lurking in the shadows

9. 📜 **Transformation Report (Optional)**
   - Summary of all steps performed

---

## 📈 Visual Add-Ons

```python
from autosage.visuals import plot_missing, plot_distribution, correlation_heatmap
```

Spells that reveal:
- Missing value shadows
- Feature distribution echoes
- Hidden correlations

---

## 🧙 Roadmap of the Enchanter

- [x] Design the spellbook structure
- [x] Add tabular visualization (including JSON parsing)
- [x] Implement AI-based Advisor module
- [ ] Implement missing value handler
- [ ] Build smart encoder and scaler
- [ ] Craft the `fit_transform()` logic
- [ ] Summon feature generators
- [ ] Add insightful visuals
- [ ] Create spell logs and transformation reports
- [ ] Release to PyPI

---

## 🧙‍♂️ Who This Is For

- Practicing data scientists seeking to save time and effort
- Aspiring wizards of ML who want preprocessing to *just work*
- Rapid prototypers and hackathon heroes who crave speed

---

## ⚡ Example Usage

```python
from autosage import Sage

sage = Sage(
    handle_missing='smart',
    encode='auto',
    scale='zscore',
    generate_features=True,
    log_steps=True
)

clean_df = sage.fit_transform(df, target='Churn')
```

---

> May your features be sharp, your noise be silent, and your models be ever wise.  
> — *The Book of Sage, Page 1.*

