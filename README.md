# Dubai Real Estate Analytics: Infrastructure-Impact Prediction Model

## Overview
This repository contains the complete codebase and analysis for a predictive analytics project examining Dubai's real estate market from 2007-2024, with forecasts through 2030. The project focuses on quantifying how planned transportation infrastructure affects property values - an impact traditional models consistently underestimate.

Using advanced machine learning techniques and geospatial analysis, we developed a hybrid LSTM-ARIMA model with infrastructure adjustments that identified significant investment opportunities in areas surrounding planned metro lines, road expansions, and other transportation projects.

## Key Findings
- Transportation infrastructure factors account for 32% of property price determinants in Dubai
- Traditional forecasting models systematically undervalue areas near planned infrastructure
- Areas like Nad Shamma show 77-103% higher ROI when infrastructure effects are properly accounted for
- Several areas with negative baseline growth projections emerge as strong investment opportunities when adjusted for upcoming infrastructure projects
- The Dubai Metro Blue Line demonstrates the highest impact coefficient, followed by road network expansion

## Dataset
The analysis uses a dataset of 300000+ property transactions across 34 Dubai neighborhoods, including:
- Transaction records (2007-2024)
- Property attributes (size, rooms, amenities)
- Geocoded property locations
- Distances to current and planned infrastructure
- Infrastructure project completion timelines

## Repository Structure
- `/data`: Raw and processed datasets
- `/notebooks`: Jupyter notebooks for analysis
  - `1_data_preparation.ipynb`: Data cleaning and preprocessing
  - `2_exploratory_analysis.ipynb`: EDA and feature importance
  - `3_arima_modeling.ipynb`: Time series forecasting
  - `4_lstm_modeling.ipynb`: Deep learning implementation
  - `5_hybrid_model.ipynb`: Combined model with infrastructure adjustments
- `/src`: Python modules and utility functions
- `/visualizations`: Generated charts and maps
- `/results`: Model outputs and findings

## Technologies Used
- **Python** (3.8+)
- **Data Processing**: Pandas, NumPy
- **Machine Learning**: Scikit-learn, TensorFlow, Statsmodels
- **Geospatial Analysis**: GeoPandas, Haversine
- **Visualization**: Matplotlib, Seaborn, Plotly, Folium

## Setup and Usage

### Prerequisites
```
pandas==1.3.5
numpy==1.21.6
scikit-learn==1.0.2
tensorflow==2.8.0
statsmodels==0.13.2
matplotlib==3.5.1
seaborn==0.11.2
plotly==5.6.0
```

### Installation
```bash
git clone https://github.com/yourusername/dubai-real-estate-analytics.git
cd dubai-real-estate-analytics
pip install -r requirements.txt
```

### Running the Analysis
1. Execute notebooks in numerical order
2. Core configuration parameters can be modified in `config.py`
3. Run full pipeline with `python src/main.py`

## Challenges Overcome
This project addressed several significant challenges:
- Missing property attributes (imputed based on area correlations)
- Absent geographic coordinates (manually geocoded 1,800+ properties)
- Creation of distance metrics to planned infrastructure projects
- Time series limitations in neighborhoods with sparse data
- Modeling transport impact through a hybrid approach when traditional models failed


## Acknowledgments
- Dubai Land Department for real estate transaction data

---

**Note**: This repository contains academic research and should not be considered financial advice. Investment decisions should incorporate additional factors beyond this analysis.
