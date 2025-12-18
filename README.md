# Weather Impact on Grocery Sales of Corporicion Favorita in Ecuador
The goal of this repository is to explore, model, and forecast how weather conditions and climate variability affect retail sales and consumer demand of grocery sales in a supermarket chain in Ecuador. This work integrates forecasting methods, consumer behavior theory, and real-world empirical evidence to provide insights for data-driven retail strategy.

## Project Description
The analysis examines the effects of weather— including temperature, precipitation — on retail performance and forecasting. It uses regression models to find out the relationship that exists between weather and grocery sales. The project further random forest model to find out the categories of grocery products that is most sensitive to changes in weather.

Key objectives include:
- Measure the quantitative relationship between daily average temperature, daily precipitation (mm), and the daily unit sales of grocery products in Ecuador. 
- Determine those product categories that are highly sensitive to weather fluctuations. 
- Apply findings from the research to develop operational guidelines for retailing in the areas of inventory control and promotion. 

## Data Collection

The analysis integrates multiple daily-level data sources:

- Grocery sales data across product families  
- Historical weather data (temperature and precipitation)  
- Retail control variables, including promotion activity and public holidays  

All datasets are temporally aligned at the daily level.

## Data Preparation & Feature Engineering

Key preprocessing steps include:

- Cleaning and merging sales and weather datasets  
- Handling missing values in critical variables  
- Computing **average daily temperature** from daily minimum and maximum values  
- Categorising weather conditions:
  - **Temperature:** Low, Normal, High (based on deviation from the mean)
  - **Rainfall:** No Rain, Light, Moderate, Heavy  
- One-hot encoding of categorical weather variables with defined baseline categories  

## Exploratory Data Analysis (EDA)

Exploratory analysis was conducted to understand data patterns and relationships:

- Distributional analysis of sales and weather variables  
- Visual comparison of sales across weather categories  
- Preliminary assessment of linear and nonlinear weather–sales relationships  

## Model Development

Two complementary modelling approaches were applied.

### Regression Analysis (OLS Regression)

- Ordinary Least Squares (OLS) regression used to estimate the effect of weather on sales  
- Weather modelled using both continuous and categorical specifications  
- **Controlled models include promotion activity and holiday indicators**  
- Normal temperature and no-rain days used as baseline reference categories  

### Machine Learning Analysis (Random Forest)

- Random Forest regression used to capture nonlinear weather effects  
- Promotion and holiday effects removed using **residualisation** before modelling weather  
- Models trained separately for each product family  

---

## Model Evaluation

Model performance was evaluated using:

- **R² (coefficient of determination)**  
- **Root Mean Squared Error (RMSE)**  

Random Forest models were assessed using a train–test split and compared across product families.

---

## Insights & Interpretation

- Quantifies how weather conditions influence daily grocery sales  
- Identifies product families most sensitive to weather variation  
- Highlights the importance of controlling for promotions and holidays  
- Combines interpretability from regression with flexibility from machine learning  

---
## Results
### OLS Regression Results

- Ordinary Least Squares (OLS) regression was used to estimate the impact of weather conditions on daily grocery sales while controlling for promotion activity and public holidays.
- Weather effects vary depending on whether temperature and rainfall are modelled as continuous or categorical variables.
- Relative to normal temperature days, extreme temperature conditions (low or high) caused decrease in sale volume
- Higher rainfall intensity is generally linked to higher sales when compared to no-rain days.

## Random Forest Results

- Random Forest models were applied to capture nonlinear weather effects after removing the influence of promotions and holidays through residualisation.

- Model performance varies across product families, indicating differences in sensitivity to weather conditions.

- R² values indicate that weather has a meaningful influence on sales.

## Feature Importance

Feature importance analysis from the Random Forest models shows that:

- Average daily temperature consistently contributes more to predictive performance than rainfall.

- Rainfall plays a secondary but still relevant role for specific product families.

- These findings complement the regression results and support the presence of nonlinear weather effects.

 
