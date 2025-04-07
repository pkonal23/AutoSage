autosage/
│
├── __init__.py                  # Expose Sage interface
├── Sage.py                      # One-command API (fit_transform)
│
├── core/                        # Core analysis logic
│   ├── __init__.py
│   ├── analyzer.py              # Data type recognition, null/missing profiling
│   └── summary.py               # EDA summaries, column stats
│
├── preprocess/                  # Preprocessing magic
│   ├── __init__.py
│   ├── missing_handler.py       # Smart missing value treatment
│   ├── encoder.py               # Categorical encoding logic
│   ├── scaler.py                # Scaling numerical features
│   └── outlier_handler.py       # Outlier detection and treatment (optional)
│
├── features/                    # Feature engineering
│   ├── __init__.py
│   ├── datetime_features.py     # Extract year/month/day, etc.
│   ├── text_features.py         # Word count, length, NLP stubs
│   ├── interaction_terms.py     # Feature combinations
│   └── selector.py              # Feature selection, pruning
│
├── visuals/                     # EDA and post-processing plots
│   ├── __init__.py
│   ├── missing_plot.py          # Heatmap for nulls
│   ├── distribution_plot.py     # Histograms, KDEs
│   └── correlation.py           # Correlation matrix
│
├── viewer/                      # Tabular views
│   ├── __init__.py
│   ├── tabular_json.py          # Convert nested JSONs to readable tables
│   └── dataframe_viewer.py      # Fancy pandas viewing for notebook/display
│
├── advisor/                     # AI insight module
│   ├── __init__.py
│   └── ai_advisor.py            # LLM or rule-based system for guidance
│
├── magic/                       # Internal orchestration
│   ├── __init__.py
│   ├── pipeline.py              # Pipeline composition
│   ├── logger.py                # Step logging and reporting
│   └── config.py                # Default config for preprocessing
│
└── utils/                       # Common helpers
    ├── __init__.py
    ├── schema_validator.py      # Schema checkers for JSON/data
    └── helpers.py               # Misc utility functions
