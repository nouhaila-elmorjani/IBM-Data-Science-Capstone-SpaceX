# IBM Data Science Capstone Project - SpaceX

## Introduction
This capstone project predicts whether the Falcon 9 first stage will land successfully. SpaceX offers Falcon 9 launches at $62 million - significantly lower than competitors charging over $165 million - primarily due to rocket reusability. Accurate landing predictions enable precise launch cost estimation for companies bidding against SpaceX.

## Business Problem
**Predict first stage landing success to determine launch costs.** By accurately forecasting landing outcomes, competing startups can make informed bids against SpaceX, leveraging cost insights derived from reusable rocket economics.

## Objectives
- Apply data science and machine learning to predict first stage landing success
- Perform comprehensive data exploration and visualization
- Develop accurate classification models to determine launch costs
- Deliver actionable insights through interactive dashboards

## Methodology

### 1. Data Collection
**SpaceX API Integration**
- REST API calls to `api.spacexdata.com/v4/launches`
- JSON response parsing and normalization
- Structured data extraction using custom functions

**Web Scraping**
- BeautifulSoup parsing of Wikipedia Falcon 9 launch records
- HTML table extraction and conversion to pandas DataFrame
- Data validation and integration with API dataset

### 2. Data Wrangling & Cleaning
- Filtered dataset to Falcon 9 launches only
- Handled missing values using mean imputation
- Standardized data formats and column names
- Created landing outcome labels for machine learning

### 3. Exploratory Data Analysis
**SQL Analysis**
- Database integration and structured querying
- Launch site performance analysis
- Payload mass and orbit type correlations

**Visual Analytics**
- Success rate trends (2010-2020)
- Orbit type performance comparisons
- Launch site reliability analysis
- Interactive Folium maps and Plotly Dash dashboard

### 4. Machine Learning Prediction
**Model Development**
- Multiple classification algorithms: Decision Tree, KNN, Logistic Regression, SVM
- Hyperparameter tuning using GridSearchCV
- Train-test split and cross-validation

**Performance Results**
- **Decision Tree & KNN**: 94.44% accuracy
- **Logistic Regression & SVM**: 83.33% accuracy
- Confusion matrix analysis for model evaluation

## Key Findings

### Launch Performance Insights
- **CCAFS LC-40**: Highest success rate (43.7%)
- **FT Booster Version**: Most reliable across payload ranges
- **Success Rate Trend**: Significant improvement from 2013-2020
- **Optimal Orbits**: ES-L1, GEO, HEO, SSO show near-perfect success rates

### Predictive Modeling
- Decision Tree and KNN models achieved highest accuracy (94.44%)
- Minimal false positives/negatives in confusion matrices
- Reliable landing outcome predictions for cost estimation

## Repository Structure
```
├── notebooks/
│   ├── Data Collection API.ipynb
│   ├── Data Collection with Web Scraping.ipynb
│   ├── Data Wrangling.ipynb
│   ├── EDA with Data Visualization.ipynb
│   ├── EDA with SQL.ipynb
│   └── Machine Learning Prediction.ipynb
├── dash_app/
│   └── app.py (Plotly Dash application)
│   └── spacex_launch_geo.csv
└── README.md
```

## Technologies Used
- **Python**: pandas, numpy, scikit-learn, BeautifulSoup
- **Data Visualization**: Matplotlib, Seaborn, Plotly, Folium
- **Machine Learning**: Decision Trees, KNN, SVM, Logistic Regression
- **Database**: SQL, Db2 integration
- **Dashboard**: Plotly Dash for interactive analytics

## Business Impact
The predictive models enable accurate launch cost estimation by determining reusable rocket viability. Companies can bid competitively against SpaceX with data-driven cost projections, potentially saving millions through informed decision-making.

## Acknowledgments
- IBM for the Data Science Professional Certificate curriculum
- Coursera for the learning platform
- SpaceX for making launch data publicly available

---

*This project demonstrates end-to-end data science capabilities from data collection to deployment-ready predictive models, providing valuable business intelligence for the commercial space industry.*
