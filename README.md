# IBM-Data Science Capstone SpaceX Falcon 9 First Stage Landing Prediction

## Project Overview
Commercial space flight is a highly competitive industry. SpaceX advertises Falcon 9 rocket launches at a cost of $62 million, significantly lower than other providers whose costs can exceed $165 million. A primary driver of these cost savings is SpaceX's ability to successfully land and reuse the first stage of the Falcon 9 rocket. 

The objective of this project is to determine the factors that influence a successful first-stage landing and to build machine learning models capable of predicting the landing outcome. Accurately predicting this outcome allows for highly accurate estimations of launch costs, providing a competitive edge for alternative companies bidding against SpaceX.

## Methodologies
This project follows a complete data science pipeline, from data extraction to predictive modeling:

1. **Data Collection:** 
   - Extracted historical launch data utilizing the SpaceX REST API.
   - Web scraped Falcon 9 launch records from Wikipedia using BeautifulSoup.
2. **Data Wrangling:** 
   - Cleaned the dataset, handled missing values, and applied one-hot encoding to categorical features.
3. **Exploratory Data Analysis (EDA):** 
   - Analyzed data trends using Python visualization libraries (Matplotlib, Seaborn).
   - Executed SQL queries to extract key metrics (e.g., total payload mass, success rates by orbit type).
4. **Interactive Visual Analytics:** 
   - Built interactive maps using Folium to analyze launch site proximities to coastlines and infrastructure.
   - Developed an interactive Plotly Dash dashboard with dropdowns and range sliders to explore success rates by site and payload mass.
5. **Predictive Analysis:** 
   - Trained and evaluated multiple classification models (Logistic Regression, Support Vector Machines, K-Nearest Neighbors, and Decision Trees).
   - Utilized GridSearchCV for hyperparameter tuning to optimize model accuracy.

## Technologies Used
* **Programming Language:** Python
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Collection:** Requests, BeautifulSoup
* **Database & Querying:** SQL, SQLite / Db2
* **Data Visualization:** Matplotlib, Seaborn, Folium, Plotly Dash
* **Machine Learning:** Scikit-Learn

## Repository Structure
* `data_collection_api.ipynb` - Data extraction via SpaceX API.
* `data_collection_web_scraping.ipynb` - Data extraction via Wikipedia scraping.
* `data_wrangling.ipynb` - Data cleaning and feature engineering.
* `eda_dataviz.ipynb` - Exploratory Data Analysis using Matplotlib and Seaborn.
* `eda_sql.ipynb` - Exploratory Data Analysis using SQL queries.
* `interactive_map_folium.ipynb` - Geospatial analysis of launch sites.
* `dashboard_plotly_dash.py` - Source code for the interactive Dash application.
* `predictive_analysis_classification.ipynb` - Machine learning model training, tuning, and evaluation.
* `Presentation.pdf` - The final executive presentation summarizing methodologies and findings.

## Key Findings
* **Launch Site Influence:** Launch site geography heavily influences success. The KSC LC-39A site accounted for the highest volume of successful launches.
* **Payload & Orbit:** Missions to VLEO, ES-L1, GEO, HEO, and SSO orbits achieved perfect success rates. Heavy payloads (above 10,000 kg) demonstrated a higher degree of variance in landing success.
* **Model Performance:** The Decision Tree classification model proved to be the most accurate predictor of landing success, achieving an accuracy of 94.44% on the test dataset.

## Author
**Hamza Ali Khan**
Date: September 2026
