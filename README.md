# FIFA-Position-Classifier


This project uses machine learning to classify soccer players into their field positions using FIFA video game statistics. It includes two models:

- **Genreica Player Position Model**: Classifies players into 4 **generic positions** (Goalkeeper, Defender, Midfielder, Attacker)
- **Specific Player Position Model**: Classifies players into 15 **specific positions** (CB, LB, CDM, CAM, ST, GK, etc.)

The project is built with Python, pandas, scikit-learn, and XGBoost, with a Quarto website for documentation and results.

---

## Project Goals

- Build multiclass classifiers to predict player positions based on FIFA attributes
- Evaluate performance using accuracy, F1-score, and confusion matrices
- Analyze feature importances to understand what attributes define each position
- Create a transparent and reproducible machine learning pipeline

---

## Data Sources

- [Sofifa](https://sofifa.com/): Primary source for player stats and ratings
- [Kaggle FIFA Dataset](https://www.kaggle.com/stefanoleone992/fifa-23-complete-player-dataset): Convenient CSVs for multiple years
- Custom mappings for generic position categories

---

## Project Structure
```{plaintext}
fifa-position-classifier/
│
├── code/
│   ├── data_preprocessing.ipynb  # Data cleaning and feature engineering
│   ├── eda.ipynb                 # EDA and data visualization
│   ├── model_generic.ipynb       # Train generic position model
│   ├── model_specific.ipynb      # Train specific position model
|
├── data/
│   ├── raw/                      # Original downloaded CSVs
│   ├── processed/                # Cleaned and feature-engineered data

├── img/                          # Visualizations and figures used in the project                                      
│
├── models/                       # Trained models and their metadata
|
├── website/
│   ├── img/                      # Static visualizations used across the website
│   ├── scripts/                  # Optional: Any JavaScript for interactivity or data handling on the site
│   ├── data_collection.qmd       # Details on FIFA data sources, scraping/preprocessing, and feature selection
│   ├── index.qmd                 # Project overview, motivation, and summary
│   ├── methods.qmd               # Model architecture, training pipeline, and evaluation metrics
│   ├── results.qmd               # Model performance, visualizations, feature importances, and discussion
│
├── README.md
└── .gitignore

```